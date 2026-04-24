# Content Page Standard

Use this document as the strict authoring standard for public pages on this math site.

The goal is consistency, clarity, and freshness. Every contributor should be able to open a template, fill the same metadata fields, follow the same writing order, and leave a page in a reviewable state.

## Non-Negotiable Workflow

### 1. Do a source sweep first

Before drafting or revising a page, check live sources.

Minimum mix:

- `1 primary source`: official course page, author-maintained notes, canonical text, or venue page
- `1 second perspective`: alternative notes, open text, or strong explainer
- `1 bridge source`: application note, survey, tutorial, or representative paper

For fast-moving pages such as `paper-lab`, `research-direction`, or `publication`, also check at least one recent source or venue page.

Record:

- title
- URL
- why it is included
- access date

### 2. Pick one page type

Use exactly one of the templates in [contributing/templates](templates/README.md).

Do not merge `concept`, `proof`, `application`, and `paper-lab` into one page. One page should have one main job.

### 3. Fill front matter before writing

Set the page metadata first so the page is classifiable, reviewable, and easy to list later.

### 4. Draft in the required section order

The section order is part of the product. Readers should learn what to expect from each page type.

### 5. Add the bridges

Every published page must connect the math to:

- at least one application or concrete use
- at least one paper, survey, or theorem-heavy note
- at least one good next resource

### 6. Decide whether code belongs inline or in a lab

If a page needs substantial code, parameter sweeps, simulations, or interactive visuals, split that material into a `computation-lab` page rather than overloading a concept or proof page.

Use short inline code only when it helps explain the page's main narrative.

### 7. Review freshness before publish

Update:

- `last-reviewed`
- `source-check-date`
- `review-cadence`
- `update-status`

If the page is not ready, keep it `draft: true`.

## Metadata Contract

Every published content page should carry this minimum front matter.

```yaml
---
title: "Page Title"
description: "One-sentence summary used in listings and search."
page-type: concept
status: published
update-status: current
level: foundation
topic: linear-algebra
prerequisites:
  - /topics/foundation/linear-algebra/index.qmd
learning-goals:
  - "State the core object or theorem precisely."
  - "Connect the idea to one application."
applications:
  - machine-learning
  - optimization
keywords:
  - linear algebra
  - vectors
maintainer: mtuann
last-reviewed: 2026-04-24
source-check-date: 2026-04-24
review-cadence: annual
date-modified: last-modified
draft: false
---
```

### Required Fields

- `title`
- `description`
- `page-type`
- `status`
- `update-status`
- `level`
- `topic`
- `prerequisites`
- `learning-goals`
- `applications`
- `keywords`
- `maintainer`
- `last-reviewed`
- `source-check-date`
- `review-cadence`
- `date-modified`
- `draft`

### Recommended Optional Fields

```yaml
next:
  - /topics/foundation/linear-algebra/concepts/orthogonality-and-least-squares.qmd
related-pages:
  - /applications/index.qmd
research-tags:
  - spectral-methods
  - generalization
stable-sources:
  - "MIT 18.06SC Linear Algebra"
current-sources:
  - "Recent survey or venue page checked online"
execution-engine: python
interactive: ojs
reproducibility-note: "Seeded simulation; all outputs render to static HTML."
sources:
  - kind: course
    label: First pass
    title: "MIT 18.06SC Linear Algebra"
    url: "https://ocw.mit.edu/courses/18-06sc-linear-algebra-fall-2011/"
    last-checked: 2026-04-24
  - kind: notes
    label: Second pass
    title: "Hefferon, Linear Algebra"
    url: "https://hefferon.net/linearalgebra/"
    last-checked: 2026-04-24
```

Keep detailed discussion of resources in the body under `Sources and Further Reading`. Use metadata only for structured tracking.

In the page body, every recommended learning resource should be labeled exactly once as `First pass`, `Second pass`, or `Paper bridge`.

## Controlled Values

### `page-type`

- `module-overview`
- `concept`
- `proof`
- `exercise`
- `application`
- `paper-lab`
- `computation-lab`
- `research-direction`
- `publication-workflow`
- `source-guide`
- `publication`
- `note`

### `status`

- `draft`
- `published`
- `archived`

### `update-status`

- `current`
- `monitor`
- `needs-refresh`
- `major-refresh`

### `level`

- `repair`
- `foundation`
- `advanced`
- `research`

### `review-cadence`

- `quarterly`
- `semiannual`
- `annual`

## Freshness Policy

Use both of these fields and do not confuse them:

- `last-reviewed`: last human content review
- `date-modified: last-modified`: Quarto-supported file change timestamp

`last-reviewed` answers: "When did someone validate correctness, clarity, and references?"

`date-modified` answers: "When did the file itself last change?"

### Default Review Cadence

| Page Type | Default Cadence | Why |
|---|---|---|
| `foundation` concepts and proofs | `annual` | Core math changes slowly |
| `advanced` topic pages | `semiannual` | Content is stable, but better references appear |
| `computation-lab` pages | `semiannual` | Code, dependencies, and visuals drift faster than core exposition |
| `application` pages | `semiannual` | Tools and examples drift |
| `paper-lab` pages | `quarterly` | Research framing ages quickly |
| `research-direction` pages | `quarterly` | New papers and venue patterns appear often |
| `publication` pages | `quarterly` | Norms and examples shift |
| `source-guide` pages | `semiannual` | Links and course pages move |

When reviewing a page:

1. re-check links
2. replace dead or stale references
3. update `last-reviewed`
4. update `source-check-date`
5. keep `update-status` honest

## Example Front Matter Blocks

### Concept Page

```yaml
---
title: "Orthogonality and Least Squares"
description: "How orthogonality turns approximation into projection and powers least-squares methods."
page-type: concept
status: published
update-status: current
level: foundation
topic: linear-algebra
prerequisites:
  - /topics/foundation/linear-algebra/concepts/vectors-and-linear-combinations.qmd
learning-goals:
  - "Recognize orthogonality as a geometric constraint."
  - "Derive the least-squares normal equations."
  - "Connect projection to regression and approximation."
applications:
  - regression
  - signal-processing
  - optimization
keywords:
  - orthogonality
  - least squares
  - projection
maintainer: mtuann
last-reviewed: 2026-04-24
source-check-date: 2026-04-24
review-cadence: annual
date-modified: last-modified
draft: false
---
```

### Paper Lab Page

```yaml
---
title: "Paper Lab: A Theory Paper on Generalization"
description: "A guided reading page that maps assumptions, claims, proof tools, and follow-up directions."
page-type: paper-lab
status: published
update-status: monitor
level: research
topic: learning-theory
prerequisites:
  - /topics/advanced/index.qmd
learning-goals:
  - "Identify the paper's core claim and assumptions."
  - "Map the proof to prerequisite math."
  - "See what has changed since publication."
applications:
  - machine-learning-theory
keywords:
  - generalization
  - paper reading
  - theory
maintainer: mtuann
last-reviewed: 2026-04-24
source-check-date: 2026-04-24
review-cadence: quarterly
date-modified: last-modified
draft: false
---
```

## Contributor Checklist

Every page revision should satisfy all of these:

- `metadata complete`
- `source sweep completed`
- `last-reviewed updated`
- `source-check-date updated`
- `review cadence set`
- `update-status honest`
- `notation introduced before use`
- `at least one worked example included`
- `at least one application or paper bridge included`
- `prerequisites and next links checked`
- `if code appears, the static render path is clear`
- `if randomness appears, seeds or stochastic assumptions are documented`
- `if figures appear, axes, legends, and control meanings are labeled`
- `draft flag correct`

## Computational Content Policy

Code, simulation, and visualization are part of the teaching product, but only when they clarify the math.

Use computational content to:

- visualize a structure that is hard to see from equations alone
- compare theory against approximation or numerics
- show the effect of assumptions, parameters, or noise
- give the reader one reproducible bridge from formal math to practice

Do not use computational content to replace exposition.

### Preferred Delivery Order

For a GitHub Pages deployment, prefer:

1. pre-rendered `Python`, `R`, or `Julia` outputs for figures and tables
2. client-side `Observable JS` for lightweight interactive visuals
3. `Jupyter Widgets` or `htmlwidgets` only when they render cleanly in static HTML

Avoid making a core page depend on a live server or hidden notebook state.

### Inline Versus Standalone

Keep code inline when:

- the code block is short
- the figure or calculation is tightly tied to one paragraph
- the reader does not need to vary many controls

Use a `computation-lab` page when:

- there are multiple parameters or controls
- the page needs a simulation, animation, or parameter sweep
- reproducibility details would distract from the main concept page
- the visual is central enough to deserve interpretation and cautions of its own

### Minimum Requirements For Every Computational Artifact

Every serious code, simulation, or visualization block must state:

- `what mathematical question it is answering`
- `what is being varied`
- `what the reader should observe`
- `what assumptions or numerical choices matter`
- `how the result connects back to the formal content`

If randomness is present, give a seed or explain the stochastic setup.

If a figure is present, label:

- axes
- units or normalization when relevant
- legend entries
- important control or parameter meanings

### Reproducibility Rule

If a reader cannot tell how the figure or simulation was generated, the artifact is not ready.

At minimum, document:

- execution engine when relevant
- seed when relevant
- key package or library names when they affect interpretation
- whether the output is pre-rendered or interactive

### House Rule

A concept page may link to a lab.
A proof page may reference a lab.
An application page may embed one small figure.
But any page that becomes code-heavy should be split into a paired `computation-lab`.

## Page-Type Rules

### `module-overview`

Required sections:

1. `Why This Module Matters`
2. `Prerequisites`
3. `What You Will Learn`
4. `Module Map`
5. `Core Concepts`
6. `Proof Patterns In This Module`
7. `Applications`
8. `Paper Bridge`
9. `Study Order`
10. `Sources and Further Reading`

### `concept`

Required sections:

1. `Role`
2. `Why It Matters`
3. `Prerequisite Recall`
4. `Intuition`
5. `Formal Core`
6. `Worked Example`
7. `Computation Lens`
8. `Application Lens`
9. `Paper Bridge`
10. `Common Mistakes`
11. `Exercises`
12. `Sources and Further Reading`

### `proof`

Required sections:

1. `Claim`
2. `Why This Proof Matters`
3. `Dependencies`
4. `Strategy Before Details`
5. `Full Proof`
6. `Step Annotations`
7. `Why The Assumptions Matter`
8. `Common Failure Modes`
9. `Reusable Pattern`
10. `Where This Shows Up Again`
11. `Exercises`
12. `Sources and Further Reading`

### `exercise`

Required sections:

1. `Scope and Goals`
2. `Prerequisites`
3. `Warm-Up Problems`
4. `Core Problems`
5. `Proof Problems`
6. `Computational or Applied Problems`
7. `Hints`
8. `Full Solutions`
9. `Common Errors`
10. `What To Do Next`
11. `Sources and Further Reading`

### `computation-lab`

Required sections:

1. `Lab Goal`
2. `Math Question`
3. `Model or Setup`
4. `Parameters and Controls`
5. `Code and Simulation`
6. `What To Observe`
7. `Interpretation`
8. `Failure Modes and Numerical Cautions`
9. `Reproducibility Notes`
10. `Extensions`
11. `Sources and Further Reading`

### `application`

Required sections:

1. `Problem Setting`
2. `Why This Math Appears`
3. `Math Objects In Use`
4. `Worked Walkthrough`
5. `Implementation or Computation Note`
6. `Failure Modes`
7. `Paper Bridge`
8. `Sources and Further Reading`

### `paper-lab`

Required sections:

1. `Why This Paper`
2. `What To Know First`
3. `First Pass`
4. `Second Pass`
5. `Math Dependency Map`
6. `Key Claims and Evidence`
7. `What To Reproduce`
8. `What Has Changed Since Publication`
9. `Sources and Further Reading`

### `research-direction`

Required sections:

1. `Direction Summary`
2. `Why It Matters`
3. `Core Math`
4. `Representative Problems`
5. `Representative Venues`
6. `Starter Reading Trail`
7. `Open Questions`
8. `What To Learn Next`
9. `Sources and Further Reading`

### `publication-workflow`

Required sections:

1. `Workflow Goal`
2. `Inputs Required`
3. `Decision Checkpoints`
4. `Step-By-Step Process`
5. `Quality Bar`
6. `Common Failure Modes`
7. `Reproducibility And Artifact Expectations`
8. `Mini Template Or Checklist`
9. `Sources and Further Reading`

## Directory Defaults

When many pages in one folder share metadata, move shared fields into `_metadata.yml`.

Example:

```yaml
level: foundation
topic: linear-algebra
review-cadence: annual
maintainer: mtuann
```

Quarto merges `_quarto.yml`, directory `_metadata.yml`, and page front matter, with page front matter taking priority.

## References

- [Quarto Front Matter](https://quarto.org/docs/authoring/front-matter.html)
- [Quarto Project Basics and `_metadata.yml`](https://quarto.org/docs/projects/quarto-projects)
- [Quarto Website Drafts](https://quarto.org/docs/websites/website-drafts.html)
- [Quarto Document Listings](https://quarto.org/docs/websites/website-listings.html)
- [Quarto Dates and `last-modified`](https://quarto.org/docs/reference/dates.html)
- [Quarto Interactivity Overview](https://quarto.org/docs/interactive/)
- [Quarto Observable JS](https://quarto.org/docs/interactive/ojs/)
- [Quarto Code Cells: Observable JS](https://quarto.org/docs/reference/cells/cells-ojs.html)
- [Quarto Jupyter Widgets](https://quarto.org/docs/interactive/widgets/jupyter.html)
- [Quarto htmlwidgets](https://quarto.org/docs/interactive/widgets/htmlwidgets.html)
- [GitHub Pages custom workflow publishing](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [GitHub Actions scheduled workflows](https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows)
