# Audit report

Produced in audit mode, and on request in rewrite mode when the user asks what changed. The default output of rewrite mode is the rewritten document alone.

Keep the report shorter than the document it describes. The point is to let the person act, not to document the process.

## Format

```
Verdict: <one sentence: where this stands and what class of problem it has>

Fails the substitution test
- "<line>". <who else could write this, specifically>
- ...

Missing evidence
- "<line>". <what number or scale would fix it, and where they would plausibly find it>
- ...

AI tells
- <pattern name and number>: <where it appears, quoted short>
- ...

Structure and convention
- <anything wrong with order, length, section balance, or surface convention>

Working already
- "<line>". <why it works>
- ...

Biggest single lift: <the one change worth doing first, and what it is worth>
```

Drop any section that is empty rather than writing "none found" under it. An audit with four headings and one line under each reads as thorough. An audit with six headings and three "none" entries reads as a form.

Four to eight lines total for a single role or a README. Twelve to twenty for a full resume. Past that, you are rewriting in audit clothing.

## Rules

**No rewriting in audit mode.** Naming the problem and saying what would fix it is the job. Showing the fixed line is the next mode, and it is the user's decision to go there. One exception: if the person explicitly asks "show me what you mean" on a single line, show that one line.

**Quote the actual line.** An audit that says "several bullets lack metrics" cannot be acted on. An audit that quotes the bullet can.

**"Working already" is not optional.** It is the half that stops the person deleting their strongest line in the next revision, and it is the half that tells them you read the document rather than pattern-matched it.

**One biggest lift.** Not a ranked list of nine. If everything is the priority, nothing is.

## Worked example

Input: two bullets from a senior analyst's resume.

> - Responsible for building and maintaining dashboards and reports for various stakeholders across the organisation
> - Leveraged SQL, Python and Tableau to deliver data-driven insights that enhanced decision-making

Output:

```
Verdict: Both bullets describe the job description rather than your performance in it, and neither carries a number. This is the most common failure mode and the most fixable.

Fails the substitution test
- "Responsible for building and maintaining dashboards and reports for various stakeholders". Every analyst who has ever held this title could write this sentence unchanged. It tells a hiring manager nothing about whether you were good at it.
- "Leveraged SQL, Python and Tableau". Those three tools appear on most analyst resumes in this market. They are table stakes, so leading with them spends your strongest line on your least differentiating fact.

Missing evidence
- Bullet 1: how many dashboards, how often refreshed, how many people or which level consumed them. A calendar invite list or the dashboard access log would tell you.
- Bullet 2: what decision actually changed because of an insight you produced. One named example beats "enhanced decision-making" entirely. Check an old performance review or a project retrospective.

AI tells
- Vague verbs (14): "Responsible for" and "Leveraged" both hide whether you did the thing or were near it.
- Forced triad (6): "SQL, Python and Tableau" is a tool list standing in for an outcome. Profile pattern P5.
- Model vocabulary (11): "leveraged", "data-driven", "enhanced", "various stakeholders".
- Unanchored claim (P4): "enhanced decision-making" has no base, no unit and no mechanism.

Structure and convention
- Two bullets for a senior role reads as thin. Three to five is the band.

Working already
- Nothing on these two lines yet. The raw material is probably fine; it has not made it onto the page.

Biggest single lift: name one decision that changed because of your work, with the scale of what it affected. That single bullet will do more than rewriting both of these.
```

## Scoring

If the user asks for a score, give one, and say what it is measured against. Never present it as an applicant tracking system score or a ranking prediction.

```
Score: 4/10 against resume convention for a senior analyst role.
Carrying it: nothing yet. Costing it: no outcomes anywhere, two bullets where five belong.
```

A score with no basis stated is worse than no score.
