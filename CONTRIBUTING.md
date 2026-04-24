# Contributing

## Contributor Sourcing Policy

This site is topic-first, not source-first. Books, courses, notes, papers, and blogs are support material for a topic page, not the topic page itself.

Every contributor must complete the sourcing checklist below before drafting or revising a topic page.

## Topic Architecture Policy

The default unit of teaching on this site is:

- `one self-contained concept page`
- `up to 3 primary companion pages`
- `optional secondary depth pages`

That means:

- a reader should be able to understand the core topic from the main concept page alone on a first pass
- the main page should answer `what is it`, `why does it matter`, and `how is it used`
- proof, application, and exercise or lab pages are the only companions that should normally feel primary
- paper-lab, research-direction, source-guide, and extra practice pages are secondary depth and should not be required for first-pass understanding

Do not split a topic into many pages unless the split changes the learning mode.

Good reasons to split:

- a full proof with its own narrative
- a distinct application reframing
- a computation lab, simulation, or visualization
- a separate paper-reading or research-direction layer

Bad reasons to split:

- the page feels long but still has one coherent teaching job
- the companion page mostly repeats the core explanation
- the topic page would become incomplete without the companion

### 1. Required Source Sweep

Before writing, check online for all changeable items:

- the current official homepage for each course you cite
- the current author or publisher page for each book you recommend
- the current status of each paper you cite if the result could have a journal version, correction, or retraction
- at least one current venue, lab, or survey page for the `research direction` section if the topic has an active modern frontier

Use the date you actually checked, not a guessed date.

### 2. Acceptable Sources

Use sources in this order of trust:

1. Official course pages, official lecture notes, official textbooks, author pages, society or publisher pages, journal pages, and conference proceedings.
2. Author-maintained surveys, open lecture notes, and serious expository notes from recognized researchers.
3. High-quality blog posts only when they add intuition or examples that stronger sources do not provide.

Blogs are never enough on their own for definitions, theorem statements, or resource recommendations.

### 3. Required Mix Per Topic Page

Every substantial topic page must include all three layers:

- `Stable core`: 2 to 5 textbooks, lecture notes, or official courses that will still make sense in a few years.
- `Current bridge`: 1 to 3 recent surveys, course notes, or official research-group pages that show how the topic is used now. `Recent` normally means within the last 3 to 5 years unless the field moves slowly.
- `Paper bridge`: 2 to 4 papers that help readers see the topic inside real research.

Do not build a page entirely from current papers. Do not build a page entirely from textbooks either. The page should teach the durable math and then point outward to active use.

### 4. Required Labels For Learning Resources

Every learning resource recommendation must be labeled exactly once:

- `First pass`: best for first exposure, intuition, notation, and basic fluency.
- `Second pass`: best for rigor, proofs, harder exercises, or a more abstract treatment after the basics are stable.
- `Paper bridge`: best used when the reader already knows the basics and wants to read theory papers, trace assumptions, or connect the topic to active research.

Do not label the same source as both `First pass` and `Second pass` unless you explain the split by chapter or section.

### 5. What Must Be Verified Online

The following must be checked online every time they are mentioned:

- course term, syllabus, and whether the course page still exists
- edition number and official access point for a book
- publication status of a paper if a preprint may have a journal or conference version
- whether a cited article has a correction, withdrawal, or retraction
- venue names, research trends, benchmark claims, and “recent direction” statements

If it can change, verify it. If you did not verify it, do not present it as current.

### 6. Citation Hygiene

Every topic page must satisfy all of these rules:

- Cite the publisher or journal version of a paper when available; include the `arXiv` version only as a supplement when it is materially easier to access or contains important exposition.
- Prefer DOI URLs in the form `https://doi.org/...` when a DOI exists.
- Include access dates for web pages, course pages, notes, and blog posts.
- Name the exact edition for books when relevant.
- Do not cite a secondary source for a theorem when you can cite the primary text or a standard reference.
- Do not copy theorem statements, explanations, or proofs closely from a source. Rewrite in the site’s voice and cite the source.
- Do not cite AI output.
- Do not recommend a source you did not inspect directly.

### 7. Balance Rules

- Stable textbooks and official notes should carry the core exposition.
- Recent surveys and official research pages should carry the `why this matters now` and `where this is going` sections.
- Papers should be used to illustrate application, style of argument, and active directions, not to replace foundational exposition.
- One exceptional resource is better than five redundant ones.

### 8. Code, Simulation, and Visualization Policy

Code, simulation, and visualization are encouraged when they clarify the math.

Use them for:

- showing a theorem-level phenomenon in action
- testing how an assumption changes behavior
- comparing exact versus approximate methods
- visualizing geometry, randomness, optimization, dynamics, or error
- giving readers a reproducible bridge from formal math to practice

Do not add code or interactivity as decoration.

For this site, prefer static-friendly or client-side approaches:

1. pre-rendered figures, tables, and outputs from `Python`, `R`, or `Julia`
2. client-side interactive visuals with `Observable JS`
3. `Jupyter Widgets` or `htmlwidgets` only when they render cleanly to static HTML

Avoid making core pages depend on a live server runtime.

Every substantial computational artifact must include:

- the exact math question it is illustrating
- the parameters or controls being varied
- what the reader should observe
- how the result connects back to a definition, theorem, assumption, or failure mode
- enough reproducibility detail to regenerate the figure or simulation

Minimum reproducibility details:

- seed if randomness is used
- parameter defaults
- runtime or engine when relevant
- external library names when they matter to interpretation

Visualization rules:

- label axes, legends, and important parameters
- state units or normalization when they matter
- do not use a visually impressive plot if a simpler one explains the math better
- do not imply a benchmark or empirical ranking claim unless it is sourced and current

### 9. Prohibited Practices

Do not:

- cite random aggregator lists, SEO articles, or unsourced summaries
- present a blog post as the authoritative source for formal content
- recommend dead links without marking them as archived
- mix incompatible notation across sources without warning the reader
- present an old paper as a `recent direction` without explaining why it is still the right reference or pairing it with a newer survey or paper
- claim a topic is important for modern research without showing at least one concrete paper, survey, or venue trail
- publish an unlabeled interactive widget with no explanation of what to vary or what to learn from it
- include stochastic simulations without fixing or documenting randomness
- rely on a server-backed demo for a page that should work on the static site

### 10. Submission Gate

A topic page is not ready to merge unless it includes:

- a `last reviewed` date
- a `sources checked online` list
- at least one `First pass`, one `Second pass`, and one `Paper bridge` resource
- at least one stable source and one current source
- citations or links for every nontrivial recommendation and every time-sensitive claim

If the page includes code, simulation, or visualization, it is also not ready unless:

- the figure, widget, or simulation has a clear teaching purpose
- the key parameters and expected observation are documented
- the artifact renders on the published static site or is clearly marked as external
- randomness, runtime assumptions, and important dependencies are documented

When in doubt, be conservative: prefer official, inspectable, durable sources and clearly mark what is current versus what is timeless.
