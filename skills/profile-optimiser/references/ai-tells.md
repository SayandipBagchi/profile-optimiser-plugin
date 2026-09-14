# Tell catalogue for profile surfaces

The pattern numbers match the `humanise` pattern catalogue, so an audit produced here is readable by anyone who knows that skill. This file covers the subset that actually shows up in resumes, LinkedIn profiles and READMEs, with examples from those surfaces.

Read it during the audit, and again before the gate.

## The ones that survive a rewrite

**1. Not X but Y.** Includes not just, not only, not merely X but Y, the reversed X rather than Y, and the contrast split across two sentences.

> Before: Not just a task tracker, but a complete workflow engine.
> After: A workflow engine with task tracking, approvals and SLA timers.

**2. Restating instead of continuing.** A closing line that repeats the line above it. On a profile this is the About section that ends with "That is what drives me."

> Before: I build payment systems at scale. Scale is the thing that matters to me.
> After: I build payment systems at scale. Currently a UK card portfolio doing four million authorisations a month.

**3. Sayings that sound deep.** "At its core", "the real question is", "what truly matters", "X is the Y of Z". Very common in a LinkedIn About opener.

> Before: At its core, product management is about empathy.
> After: I spend most of my time turning half-formed requests from six teams into one buildable roadmap.

**4. Staged run-up.** "Let me tell you about", "here is the thing", "so, a little about me". Cut the run-up and start at the point.

**6. Forced triads.** The single most common resume tell, because the mechanism turns into a list.

> Before: Led the migration through stakeholder alignment, technical design and change management.
> After: Led the migration by rebuilding the reconciliation layer first, which unblocked the other two workstreams.

Keep three items where the meaning has three parts. The bullet formula wants one mechanism, so a triad in a mechanism slot is almost always padding.

**8. Dashes.** No em dash, en dash, spaced hyphen used as a dash, or double hyphen in the output. Replace with a period, comma, colon or parentheses, or rewrite. Dashes inside code, commands, paths, URLs and flags are untouched. A dash is not evidence that a model wrote something. It still comes out of the rewrite.

**11 and 12. Model vocabulary and inflated significance.** The resume version of this list, which is slightly different from the general one:

leveraged, spearheaded (overused to the point of parody, keep only where it is accurate), passionate, driven, results-driven, dynamic, seasoned, proven track record, demonstrated ability, robust, seamless, cutting-edge, best-in-class, world-class, thought leader, game changer, synergy, holistic, strategic as a filler adjective, deep dive, delve, showcase, underscore, testament, landscape, tapestry, pivotal, crucial, key as an adjective.

The README version: blazing fast, powerful, elegant, effortless, revolutionary, simply, just, magical, batteries included used without saying which batteries.

A formal word outside these lists is not a tell on its own. These are watch lists, not blacklists. "Robust guarantee" in a technical sense is fine. "Robust solution" is not.

**13. Sales language.** A library does not "boast" a feature set and a person is not "renowned for". State what the thing is and let the reader conclude.

**14. Vague verbs.** Serves as, functions as, plays a role in, is associated with, is responsible for, is involved in, contributes to, supports, assists. Every one of these hides whether the person did the thing or watched it happen. Replace with the verb that says what happened, or ask what happened.

**16. Passive voice and missing subjects.** "The migration was completed" does not say by whom, which on a resume is the entire question. Use active voice unless the actor is genuinely irrelevant.

**17 and 18. Decoration.** Bold labels on every bullet, emoji as list markers, horizontal rules between every section, title case headings, badge walls on a README, an About section broken up with arrow characters. Remove anything that carries no navigation purpose. Keep badges that report real status such as build, coverage or version.

**19. Chatbot residue.** "I hope this helps", "Of course", "Here is your optimised resume", "Let me know if you would like". None of this belongs in a document the person will send. It also occasionally survives into the document itself when someone pastes a model's output straight in, so check the input for it.

**20. Knowledge-limit disclaimers.** "Based on available information", "details are limited". If a fact is not in the source, say what is missing or leave it out. Never fill the gap with a plausible guess, which on a resume is fabrication with extra steps.

## Profile-specific tells that are not in the general catalogue

**P1. The interchangeable opener.** Every bullet in the section starts with the same verb, usually Led or Managed. Vary by what actually happened rather than by thesaurus.

**P2. The responsibility list.** A bullet that describes the job description rather than the person's performance in it. Diagnostic: could this sentence have been copied from the posting they answered?

**P3. Scope inflation by preposition.** "Worked with the leadership team on the strategy" implies ownership without claiming it. Say what they owned. If they did not own it, say what they contributed and let it be smaller and true.

**P4. The unanchored percentage.** "Improved efficiency by 40%" with no base, no unit and no mechanism. A number with nothing under it invites exactly the question the person does not want.

**P5. Tool listing as substitute for outcome.** "Used Python, SQL, Airflow and dbt to build pipelines." The tools are the least differentiating thing on the page; hundreds of candidates list the same four. Lead with what the pipeline did.

**P6. The aspirational identity line.** "Aspiring data scientist", "transitioning into product". It tells the reader what the person is not yet. Write what they have actually done that points that way.

**P7. README philosophy first.** Three paragraphs on the motivation and design principles before a single line saying what the software does.

## When a tell is not a tell

- A dash inside a code block, a command, a flag, a path or a URL.
- Three items where the work genuinely had three parts, such as three named systems that were all migrated.
- Repetition used deliberately for rhythm in a LinkedIn About section that otherwise sounds like a person.
- Formal register in an academic CV, a legal resume or a regulated-industry profile, where it is the convention.
- An odd, very specific detail. That is almost always the strongest thing on the page.
- Text written before late 2022. Salutations, formal openers and summary paragraphs predate chat assistants and prove nothing about authorship.
