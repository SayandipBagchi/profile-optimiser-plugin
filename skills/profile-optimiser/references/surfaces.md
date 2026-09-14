# Surface guide

Four surfaces, one underlying test, different conventions. Get the surface right before you write a line, because a resume bullet dropped into a project README reads as marketing and a README paragraph dropped into a resume reads as filler.

## Resume

**Reader.** A recruiter screening 60 applications, then a hiring manager who will spend longer only if the top third of page one earns it.

**Order.** Contact block. Highlight reel. Experience. Skills. Education. Certifications. Anything else last.

**Voice.** No pronoun. Past tense for finished work, present tense for the current role. No full stops at the end of bullets is a convention, not a rule; whichever you pick, keep it consistent down the page.

**Length.** One page under ten years of experience. Two pages above it. Three only for academic or federal formats where it is the norm.

**Per role.** Two to five bullets. A role with one bullet reads as unimportant. A role with eight stops being read after the third.

**What to leave alone.** Dates, titles, company names, degrees, certifications, licence numbers, clearance levels, visa or work authorisation statements. Rewrite how work is described, never what the record says.

**Common failures.**
- Every bullet opens with the same verb.
- The most recent role gets six bullets and the role where the person actually did the interesting work gets two.
- A skills section listing twenty tools with no signal about depth.
- The summary paragraph that says "results-driven professional with a proven track record".

## LinkedIn

A profile gets read in three passes. The headline decides whether there is a second pass. The About section decides whether there is a third.

**Headline.** 220 characters. The default is your job title, which tells a reader nothing they could not get from the role entry. Better shape: what you do, who for, and one proof point or specialism. Avoid the stacked pipe format when it runs past three segments; it stops parsing on mobile.

**About.** First two lines show before the "see more" cut. Put the point there. Written in first person, because a third-person bio on LinkedIn reads as a press release. 3 to 5 short paragraphs, or a short paragraph followed by four highlight-reel lines. Close with what you want a reader to do, if you want anything.

**Experience entries.** Same bullet formula as the resume, with more room. LinkedIn tolerates a one-line role summary above the bullets. Keep the bullets to three or four per role; nobody scrolls a fifth.

**Featured, skills, recommendations.** Featured items should be things a stranger can open and evaluate in a minute. Skills should be ordered so the top three match what you want to be found for, since those are what appear by default.

**Common failures.**
- The About section is the resume summary pasted in, so it reads in third person and carries no voice.
- Buzzword clusters: passionate, driven, thought leader, innovative, dynamic.
- A headline that is only the job title.
- Emoji bullet separators that break screen readers and look dated.

**What LinkedIn tolerates that a resume does not.** First person. Personality. A short story. An opinion about the work. Use that room; it is the only one of the four surfaces where voice is an asset rather than a risk.

## GitHub profile README

**Reader.** An engineer or hiring manager who clicked your username from a pull request, an issue or a search result. They want to know what you build and where to look first.

**Shape.** Short. Ten to twenty-five lines of actual content.

- One or two lines on what you work on and at what depth.
- Three to five repositories worth opening, each with one line saying what it is and why it exists. Link them.
- What you are working on or learning now, only if it is genuinely current.
- How to reach you.

**What to cut.** Badge walls. Animated typing banners. Contribution streak widgets and trophy cards. A visitor counter. A wall of language and tool icons. These substitute decoration for information and every reviewer has seen the same template.

**What earns its place.** A specific project with a specific reason. "Built X because Y kept breaking" tells a reader more than twelve technology badges.

**Common failures.**
- Pinned repositories are tutorial forks or bootcamp exercises.
- Every project is described as "a simple app to".
- The README has more images than sentences.

## Project README

**Reader.** A developer deciding in about thirty seconds whether this repo solves their problem.

**Above the fold, in this order.**

1. What it does, in one sentence, in plain terms. Name the problem it solves.
2. Who it is for, and explicitly who it is not for.
3. The smallest working example. Install and a usage snippet that actually runs.
4. Status: maintained, experimental, archived. Say it rather than leaving it to be inferred from the commit history.

**Below the fold.** Configuration, API reference, comparison with alternatives, contributing, licence.

**Voice.** Second person for instructions ("run this"), plain declarative for description. Present tense. Describe what the project does now; a README that explains what it used to do belongs in a changelog.

**Protected content.** Code blocks, commands, paths, URLs, environment variable names, version numbers, licence text, badges that carry real status such as build and coverage. Leave every one of them exactly as supplied.

**Common failures.**
- The first paragraph explains the philosophy before saying what the thing does.
- The install section assumes a toolchain that is never named.
- Feature lists as a wall of bullets with no example.
- "Coming soon" sections that have been there for two years.
- Marketing adjectives on a library: blazing fast, powerful, elegant, seamless. Replace with the measurement or delete.

## Cross-surface consistency

When more than one surface is in scope, keep them consistent on the facts and different in register.

- Titles, dates and company names match exactly across resume and LinkedIn. A mismatch is the one thing a recruiter will actively question.
- The strongest two case-study lines can appear on both, phrased differently. The resume version is compressed, the LinkedIn version can breathe.
- A project described on the resume, in the GitHub profile and in its own README should agree on scale and outcome. Different numbers in three places reads as carelessness at best.
