# Profile optimiser

Author: Sayandip Bagchi. Version lives in `.claude-plugin/plugin.json`.

One skill and five commands, for the documents a stranger skims before deciding whether you are worth more of their time.

A resume, a LinkedIn profile, a GitHub profile README and a project README do the same job and fail the same way. The writing describes activity that a hundred other people or projects could also claim. Adding a language model to the draft makes it worse, because a model reaches for the phrasing that fits the widest range of subjects, and width is the whole problem.

**`profile-optimiser`** runs two tests over every line. The substitution test asks whether the line would still be true if you swapped in someone else with a similar background, or another project in the same category. The evidence test asks whether there is a number, a named scale, a named system or a mechanism under the claim. A line that fails both is a rewrite. A line that fails one is an upgrade. A line that passes both stays, even if it reads a little rough.

It diagnoses before it rewrites, never writes a number the person did not supply, and holds its own output to the anti-AI-tell gate so the result does not read as generated.

Status: maintained, v1.0.0. Markdown only, so there is nothing to break between Claude Code releases. Licensed proprietary; see [LICENSE](LICENSE).

## Layout

```
profile-optimiser/
├── .claude-plugin/
│   ├── plugin.json                 name, version, author. Single source of truth.
│   └── marketplace.json            makes this repo installable as a marketplace
├── commands/
│   ├── audit.md                    /profile-optimiser:audit        diagnose, no rewrite
│   ├── resume.md                   /profile-optimiser:resume       bullets and highlight reel
│   ├── linkedin.md                 /profile-optimiser:linkedin     headline, About, experience
│   ├── readme.md                   /profile-optimiser:readme       project or profile README
│   └── talk-track.md               /profile-optimiser:talk-track   what you say when asked
├── skills/profile-optimiser/
│   ├── SKILL.md                    modes, formula, evidence discipline, gate
│   └── references/
│       ├── surfaces.md             per-surface conventions and failure modes
│       ├── evidence-interview.md   question banks, estimates, confidential figures
│       ├── ai-tells.md             profile-specific tells, numbered to humanise
│       ├── audit-report.md         audit output contract, worked example
│       └── talk-track.md           spoken contract, time boxes, pushback
├── hosts/openai.yaml               optional UI metadata for OpenAI hosts
├── scripts/validate_skill.py       structural validator, stdlib only
├── evals/                          12 cases, each with prompt and graders
├── README.md, CHANGELOG.md, LICENSE
```

No `.mcp.json`, no `hooks/`, no `settings.json`, no `bin/`. Nothing here needs a connector, a hook or a binary.

## Install

From this repository, in Claude Code:

```
/plugin marketplace add sayandip1987/profile-optimiser-plugin
/plugin install profile-optimiser@profile-optimiser
```

Or clone it and add the folder as a local marketplace:

```
git clone https://github.com/sayandip1987/profile-optimiser-plugin.git profile-optimiser
```
Clone into a folder named `profile-optimiser` so `scripts/validate_skill.py` passes: it checks that the folder name matches the plugin name.
```
/plugin marketplace add ./profile-optimiser
/plugin install profile-optimiser@profile-optimiser
```

You can also drop a packaged `.plugin` file into Claude and accept it.

## Use

Claude picks the skill up on its own from phrases like "make my resume bullets stronger", "why is my LinkedIn getting nothing", "review this README", "my resume is getting no callbacks", or "what do I say when they ask about this project". Name a surface directly with the commands above.

Three modes:

- **Audit.** You pasted something and asked how it reads. It diagnoses and does not rewrite. Naming the fix is not applying it, and applying it is your decision.
- **Rewrite.** Scope, inputs, silent diagnosis, evidence interview where the outcomes are missing, then lines built on the formula and run through the gate.
- **Talk track.** The spoken version, for the screen or the interview that comes after someone reads the line.

When the request is ambiguous, it audits first. An unrequested rewrite of writing that was already working is the worst outcome the skill can produce.

## The line formula

```
[Ownership verb] + [specificity signal] + [hard result] + [single mechanism]
```

12 to 28 words. Two to five lines per role. One mechanism, never a list. No pronoun on a resume, first person on LinkedIn. The first four words and the last four words have to land on their own, because that is all most readers see.

## What it will not do

- Write a number you did not supply or confirm, including inside an illustrative example.
- Change a title, degree, credential, clearance, employment date or company name.
- Give an applicant tracking system score, a keyword guarantee, or a ranking prediction.
- Write a recommendation as though another named person wrote it.
- Rewrite a document that was already working, just to show activity.
- Take on cover letters, outreach messages, job search strategy or compensation negotiation. Those get named as out of scope and handed back.

## Why the skill is split across five references

`SKILL.md` carries the modes, the line formula, the evidence discipline and the output gate, which apply on every invocation. The five files under `references/` do not.

That split is a context decision. A resume rewrite needs `surfaces.md` for the resume conventions and `evidence-interview.md` for the question banks, and has no use for `talk-track.md`. An audit needs `audit-report.md` and `ai-tells.md` and should never load the interview banks, because it is not going to ask for numbers. Loading all five every time would spend the window describing three surfaces the request is not about, before the skill has read what the person actually pasted.

So the routing happens first and the references load second, which is also why the surface guide opens by saying to get the surface right before writing a line. Choosing the wrong reference set is a worse failure than loading slightly too little, because a LinkedIn About section rewritten under resume conventions comes back in third person with the pronouns stripped, and it reads as a press release.

## Evals

```
python3 scripts/validate_skill.py
```

Twelve cases under `evals/`, each with a prompt and two graders. Eleven expect the skill to fire; one expects it not to. They cover the appropriateness boundary the skill lives or dies on: fabricated metrics, credential and title inflation, confidential figures, tracking system claims, ghostwritten recommendations, prompt injection through a pasted job description, surface routing, audit-without-rewrite, the output tell gate, evidence discipline in a spoken answer, and doing no harm to a draft that was already strong.

The cases were written alongside the skill's specification rather than after it worked. That is why the boundary cases outnumber the capability cases: what this skill must refuse to do was decided before what it does, because a profile editor that invents a metric is worse than no profile editor. `profile-no-invented-metrics` and `profile-strong-draft-no-harm` would not have occurred to me from looking at a working rewriter, which only ever shows you the things it changed.

The graders are an LLM-as-judge setup, kept to narrow questions. `skill-fired.md` asks one binary thing. `criteria.md` checks named properties against a written rubric, one at a time, rather than returning an overall score. A judge asked whether a resume bullet is strong gives an opinion; a judge asked whether every number in the output also appears in the input gives a fact, and only the second is worth gating on. Both rubrics live next to the case they grade, so changing the bar is a reviewable diff.

## Lineage

The bullet method, the copy-paste diagnostic, the highlight reel and the metric extraction interview are adapted from the Cultivated Culture resume approach by Austin Belcak, extended to LinkedIn and README surfaces.

The pattern numbering, the final gate, the do-no-harm rule and the evidence discipline come from the `humanise` plugin, and the tells are numbered to match its catalogue so an audit from either skill reads the same way. Where `humanise` and `meeting-talk` are installed, general prose and meeting talking points route to them.
