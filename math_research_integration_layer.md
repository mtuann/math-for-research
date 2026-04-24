# Math Research Integration Layer

## Goal

This document designs the `research integration layer` for a public math learning website aimed at:

- future `PhD-level theory reading`
- `CS / AI / engineering` learners
- people who want each math topic to connect to `applications`, `papers`, and `active research directions`

The main design rule is:

`Do not isolate research into a separate island.`

Every major math topic should have embedded research hooks, while the global `research/` section acts as an aggregator and navigation layer.

## What The Research Layer Should Do

For every important topic, the site should help the reader answer five questions:

1. `What is the object or theorem?`
2. `Why does it matter in modern research?`
3. `Where is it used in applications or models?`
4. `Which papers rely on it?`
5. `Which active areas are pushing it further?`

That means each mature topic page should eventually connect:

- `topic -> theorem family`
- `topic -> application page`
- `topic -> paper lab`
- `topic -> research direction`
- `topic -> venue / survey / canonical references`

## Core Design Principles

### 1. Research should be embedded, not siloed

Each topic folder should include its own `research/` subtree. The top-level `research/` section should aggregate and cross-link those pages.

### 2. Separate stable math from moving frontier

Each page should visibly distinguish:

- `stable core`: definitions, standard theorems, canonical proofs
- `bridge layer`: surveys, lecture notes, textbook chapters, classical papers
- `frontier layer`: current directions, representative recent papers, venue watchlists

This prevents the site from becoming stale while keeping the math durable.

### 3. Prefer theorem families over isolated facts

Research papers usually rely on `stacks` of results, not single definitions. The site should therefore emphasize dependency pages such as:

- `concentration inequalities family`
- `spectral methods family`
- `convexity and duality family`
- `uniform convergence and complexity family`
- `stability and conditioning family`

### 4. Every paper page should backfill prerequisites

A paper lab should never assume the reader already knows everything. It should route back to:

- concept pages
- proof pages
- theorem dependency pages
- application pages

### 5. Every topic page should have one practical application door

Even proof-heavy topics need a concrete entry point such as:

- `SVD -> PCA / low-rank approximation`
- `convexity -> regularized ERM / constrained optimization`
- `concentration -> generalization / uncertainty / random matrices`
- `ODEs -> control / dynamics / continuous-time modeling`

### 6. Use curated paper ladders

For research-facing reading, a topic should usually expose:

- `classic`: a canonical older paper or theorem source
- `bridge`: a tutorial, survey, or course note
- `current`: a representative modern paper or workshop/conference direction

This is a better reading experience than dumping a long bibliography.

## Information Architecture

The cleanest structure is:

1. `foundations/` holds the main teaching content
2. each foundation topic gets its own `research/` subtree
3. `research/` at the root aggregates paper labs, theorem maps, applications, and directions across topics

## GitHub Pages-Friendly Constraints

If you want this to publish cleanly as a lightweight public site, the research layer should assume:

- pages are authored in `Markdown` or `MDX`
- math is rendered with `KaTeX` or `MathJax`
- dependency graphs have a `Mermaid or SVG` view plus a `text fallback`
- every page is understandable even if JavaScript-enhanced filters are unavailable
- `last reviewed` dates are plain front matter fields, not hard-coded into layout templates

In practice, that means the content model should be `static-first` and `data-light`.

The site can still become more interactive later, but the core research layer should already work as a good math website with:

- clean equations
- readable theorem maps
- searchable tags
- stable URLs

## Section Tree

### Global Content Tree

```text
content/
  roadmaps/
    core-math-foundation.md
    paper-reading-track.md
    ml-theory-track.md
    systems-track.md

  foundations/
    proofs-and-logic/
      index.md
      concepts/
      proofs/
      exercises/
      research/
        index.md
        theorem-maps/
        applications/
        paper-labs/
        directions/

    discrete-math/
      index.md
      concepts/
      proofs/
      exercises/
      research/
        index.md
        theorem-maps/
        applications/
        paper-labs/
        directions/

    linear-algebra/
      index.md
      concepts/
      proofs/
      exercises/
      research/
        index.md
        theorem-maps/
        applications/
        paper-labs/
        directions/

    calculus/
      single-variable/
      multivariable/
      research/

    odes-and-dynamical-systems/
      index.md
      concepts/
      proofs/
      exercises/
      research/
        index.md
        theorem-maps/
        applications/
        paper-labs/
        directions/

    probability/
      index.md
      concepts/
      proofs/
      exercises/
      research/
        index.md
        theorem-maps/
        applications/
        paper-labs/
        directions/

    statistics/
      index.md
      concepts/
      proofs/
      exercises/
      research/
        index.md
        theorem-maps/
        applications/
        paper-labs/
        directions/

    real-analysis/
      index.md
      concepts/
      proofs/
      exercises/
      research/
        index.md
        theorem-maps/
        applications/
        paper-labs/
        directions/

    optimization/
      index.md
      concepts/
      proofs/
      exercises/
      research/
        index.md
        theorem-maps/
        applications/
        paper-labs/
        directions/

    numerical-methods/
      index.md
      concepts/
      proofs/
      exercises/
      research/
        index.md
        theorem-maps/
        applications/
        paper-labs/
        directions/

    matrix-analysis/
      index.md
      concepts/
      proofs/
      exercises/
      research/
        index.md
        theorem-maps/
        applications/
        paper-labs/
        directions/

    learning-theory/
      index.md
      concepts/
      proofs/
      exercises/
      research/
        index.md
        theorem-maps/
        applications/
        paper-labs/
        directions/

    high-dimensional-probability/
      index.md
      concepts/
      proofs/
      exercises/
      research/
        index.md
        theorem-maps/
        applications/
        paper-labs/
        directions/

    high-dimensional-statistics/
      index.md
      concepts/
      proofs/
      exercises/
      research/
        index.md
        theorem-maps/
        applications/
        paper-labs/
        directions/

  research/
    index.md

    paper-labs/
      index.md
      by-topic.md
      by-difficulty.md
      by-venue.md

    theorem-maps/
      index.md
      by-topic.md
      proof-patterns.md

    applications/
      index.md
      machine-learning.md
      statistical-inference.md
      optimization-and-decision.md
      control-and-robotics.md
      scientific-computing.md
      signal-and-information.md

    directions/
      index.md
      learning-theory.md
      high-dimensional-inference.md
      optimization-for-ml.md
      randomized-numerical-linear-algebra.md
      control-and-sequential-decision.md
      information-theory-for-learning.md
      scientific-ml-and-inverse-problems.md

    venues/
      index.md
      theory.md
      machine-learning.md
      applied-math.md
      control.md

    surveys/
      index.md
      by-topic.md
      by-area.md
```

### Important Architectural Rule

The top-level `research/` section is an `aggregator`, not the primary home of the content.

The primary home of research content should usually be under the corresponding topic, for example:

```text
foundations/probability/research/theorem-maps/concentration-family.md
foundations/probability/research/applications/generalization-and-tail-bounds.md
foundations/probability/research/paper-labs/matrix-bernstein-lab.md
foundations/probability/research/directions/high-dimensional-probability.md
```

The global `research/` section should surface those pages through indexes, filters, tags, and graphs.

## Recommended Entry Modes

The site should support five researcher entry modes:

1. `Roadmap-first`
2. `Topic-first`
3. `Paper-first`
4. `Application-first`
5. `Direction-first`

### Roadmap-first

The learner asks:

`What should I study next?`

### Topic-first

The learner asks:

`I need to really understand concentration inequalities / SVD / convex duality.`

### Paper-first

The learner asks:

`I am reading this paper and need the hidden prerequisites.`

### Application-first

The learner asks:

`Why do low-rank methods matter for recommendation, representation learning, or compression?`

### Direction-first

The learner asks:

`What active areas use this math, and what should I read after the core?`

## Reusable Page Template System

The best system is to define a small number of reusable page types and assemble the site from them.

## Template 1: Topic Research Hub

This is the `research landing page` for a topic such as `probability`, `optimization`, or `matrix analysis`.

### Purpose

Turn a math topic into a research gateway.

### Required sections

1. `Why this topic matters in research`
2. `Core objects and notation`
3. `Theorem families`
4. `Applications`
5. `Canonical paper ladder`
6. `Active directions`
7. `Venue watch`
8. `Suggested next pages`

### Recommended page outline

```text
Title
One-paragraph overview

Why this topic matters
Core objects and notation
Research skills this topic unlocks

Theorem families
- family 1
- family 2
- family 3

Application paths
- path 1
- path 2
- path 3

Paper ladder
- classic
- bridge
- current

Active directions
- direction 1
- direction 2
- direction 3

Venue watch
Next steps
```

### Example

For `probability`, the research hub might point to:

- theorem family: `concentration inequalities`
- application page: `generalization, uncertainty, and random matrices`
- paper lab: `matrix tail bounds`
- direction page: `high-dimensional probability`

## Template 2: Theorem Dependency Page

This page is for a `theorem family` or `dependency chain`, not just a single result.

### Purpose

Show how a proof-heavy idea is built and why the stack matters in papers.

### Best use cases

- `concentration inequalities family`
- `spectral methods family`
- `convexity and duality family`
- `uniform convergence and complexity family`
- `stability and conditioning family`

### Required sections

1. `Family overview`
2. `Prerequisite graph`
3. `Main nodes`
4. `Typical assumptions`
5. `Proof patterns`
6. `What this family lets you prove`
7. `Where it appears in papers`
8. `Bridge to application pages`

### Recommended page outline

```text
Title
What this theorem family does

Dependency graph
Prerequisites in plain English

Main results
- theorem A
- theorem B
- theorem C

Typical assumptions and failure modes
Proof patterns and recurring tricks
Consequences and corollaries

Papers that rely on this family
Applications powered by this family
What to study next
```

### Render rule

Every dependency page should render in two ways:

- as a `visual graph`
- as a `text fallback adjacency list`

That keeps it usable on a simple GitHub Pages site even without heavy JavaScript.

## Template 3: Application Page

This is the `problem-first` page type.

### Purpose

Explain how math becomes leverage in a real research area or modeling problem.

### Example page titles

- `Why SVD matters for PCA and low-rank modeling`
- `Why convex duality matters for constrained learning`
- `Why concentration matters for generalization bounds`
- `Why ODEs matter for control and continuous-time models`
- `Why operator norms matter for stability and perturbation bounds`

### Required sections

1. `Problem statement`
2. `Why the math enters`
3. `Minimal math toolkit`
4. `Canonical formulations`
5. `Worked derivation or argument`
6. `Representative papers`
7. `Current extensions`
8. `Common misunderstandings`

### Recommended page outline

```text
Title
One-sentence problem definition

What the application is
Why this math matters here
Minimal prerequisite toolkit

Canonical math formulation
Worked derivation or schematic proof
Computational note

Representative papers
- classic
- bridge
- current

Where the area is moving
What to read next
```

## Template 4: Paper Lab

This is the main `paper-reading page` type.

### Purpose

Guide the learner through a research paper without letting them drown in notation or hidden prerequisites.

### Required sections

1. `Why this paper matters`
2. `First-pass summary`
3. `Second-pass theorem and notation map`
4. `Third-pass proof / method walkthrough`
5. `Hidden prerequisites`
6. `Main theorem dependency stack`
7. `One reproduction or extension task`
8. `Follow-up papers`

### Recommended page outline

```text
Title
Paper metadata

Why this paper matters
Paper type
- theorem paper
- method paper
- survey
- bridge paper

First pass
- question
- claim
- contribution
- main result in plain language

Second pass
- notation map
- theorem map
- assumptions
- proof skeleton

Third pass
- detailed walkthrough
- where the hard steps are
- what is genuinely new

Hidden prerequisites
Reproduction or extension task
Follow-up papers
Backlinks to foundation pages
```

### Paper tiers

Every paper lab should be tagged as one of:

- `P0`: tutorial, note, or expository bridge
- `P1`: classical canonical paper
- `P2`: standard graduate-level paper
- `P3`: frontier paper

That makes sequencing much smoother.

## Template 5: Research Direction Page

This is the `active area` page type.

### Purpose

Explain a living research area to someone who already has or is building the math prerequisites.

### Example page titles

- `Learning theory and generalization`
- `High-dimensional inference`
- `Optimization for machine learning`
- `Randomized numerical linear algebra`
- `Control and sequential decision-making`
- `Information-theoretic limits in learning`

### Required sections

1. `What the direction studies`
2. `Why it matters now`
3. `Entry prerequisites`
4. `Core math dependencies`
5. `Canonical surveys / notes`
6. `Representative papers`
7. `Venue watch`
8. `Open questions or tensions`

### Recommended page outline

```text
Title
Short overview

Why this area exists
What mathematical tools it uses
Prerequisites before entering

Stable backbone
- topics
- theorem families
- standard papers

Current pulse
- representative recent themes
- recent workshop / conference signals
- newer variants or debates

Where to watch
- conferences
- journals
- seminars or labs

Starter reading sequence
Open questions
```

### Important maintenance rule

Direction pages should have a visible `last reviewed` date because they are the most time-sensitive pages on the site.

## Template 6: Survey / Reading Trail Page

This page type sits between a topic page and a paper lab.

### Purpose

Offer a structured reading ladder for an area where learners need more context before reading frontier papers.

### Good uses

- `Concentration for ML theory`
- `Random matrix tools for data science`
- `Convex optimization for learning`
- `High-dimensional inference starter trail`

### Required sections

1. `What this trail prepares you for`
2. `Prerequisites`
3. `Classic -> bridge -> current ladder`
4. `Suggested stopping points`
5. `Which papers become readable after this trail`

## Reusable Building Blocks

These are the components that should repeat across templates.

### 1. Prerequisite Snapshot

Short list of the exact ideas the reader needs before this page.

### 2. Notation Map

Table or bullet list translating paper notation into familiar symbols and meanings.

### 3. Theorem Ladder

A short stack of results in dependency order.

### 4. Paper Trio

- `classic`
- `bridge`
- `current`

### 5. Application Grid

Three to six concrete use cases with one-sentence explanations.

### 6. Direction Radar

The active-area box on a topic page.

### 7. Venue Watch

A short block listing where this kind of work often appears.

### 8. Reproduction Task

One proof recreation, derivation, coding exercise, or experimental extension.

### 9. Failure Modes

A short list of common conceptual mistakes.

### 10. Backfill Links

Links back to concept, proof, and exercise pages for missing background.

## Content Graph Model

To make the site navigable, each page should expose structured relationships.

### Recommended link types

- `prerequisite_of`
- `uses`
- `used_in`
- `generalizes`
- `special_case_of`
- `appears_in`
- `applies_to`
- `related_direction`
- `watch_venue`

### Example

For `Matrix Bernstein Inequality`:

- `uses`: mgf, operator norm, PSD matrices
- `used_in`: covariance estimation, randomized linear algebra, spectral graph methods
- `appears_in`: paper labs on matrix concentration and sketching
- `related_direction`: high-dimensional probability, randomized NLA
- `watch_venue`: COLT, JMLR, ICML/PMLR, SIMAX

## Metadata Schema

Use front matter that is easy to author in Markdown and easy to index later.

```yaml
---
title: Matrix Bernstein Inequality
slug: matrix-bernstein-inequality
page_type: theorem-map
topic: probability
subtopics:
  - concentration inequalities
level: advanced
stability: stable-core
prerequisites:
  - expectation
  - mgf
  - operator norm
used_in:
  - covariance estimation
  - randomized linear algebra
  - spectral methods
related_pages:
  - concentration-inequalities-family
  - generalization-and-tail-bounds
  - matrix-tail-bounds-paper-lab
directions:
  - high-dimensional-probability
  - randomized-numerical-linear-algebra
venues:
  - colt
  - jmlr
  - pmlr
  - simax
canonical_refs:
  - tropp-user-friendly-tail-bounds
  - vershynin-high-dimensional-probability
last_reviewed: 2026-04-24
---
```

## Topic-To-Research Connection Map

This is the heart of the design. Each core topic should connect to application families and research directions in a predictable way.

### Proofs and Logic

- theorem families: implication, induction, contradiction, compact proof patterns, quantifier manipulations
- applications: theorem writing, correctness arguments, impossibility statements
- directions: theoretical CS, learning theory, formal methods
- venue watch: COLT, ALT, SIAM Journal on Computing

### Discrete Math

- theorem families: counting, graph arguments, recurrences, probabilistic method
- applications: algorithms, networks, combinatorial learning, graph ML theory
- directions: learning theory, graph methods, algorithmic foundations
- venue watch: COLT, ALT, ICML/PMLR, NeurIPS/OpenReview

### Linear Algebra

- theorem families: spectral decomposition, SVD, perturbation, low-rank approximation
- applications: PCA, embeddings, compression, latent-variable methods, graph methods
- directions: randomized numerical linear algebra, representation learning, matrix sensing
- venue watch: SIMAX, ICML/PMLR, NeurIPS/OpenReview, JMLR

### Calculus and Multivariable Calculus

- theorem families: Taylor expansions, chain rule in high dimensions, implicit viewpoints
- applications: optimization, sensitivity analysis, continuous-time modeling
- directions: optimization for ML, scientific ML, dynamical systems
- venue watch: ICML/PMLR, NeurIPS/OpenReview, SIOPT, SINUM

### ODEs and Dynamical Systems

- theorem families: stability, phase portraits, linear systems, Lyapunov-style reasoning
- applications: robotics, control, sequential decision-making, neural ODE viewpoints
- directions: control, RL theory, underactuated systems, continuous-time models
- venue watch: L4DC, CDC, SICON, Underactuated-style course ecosystems

### Probability

- theorem families: concentration, martingales, convergence, conditioning
- applications: uncertainty quantification, generalization, randomized algorithms, random matrices
- directions: high-dimensional probability, learning theory, stochastic control
- venue watch: COLT, JMLR, PMLR, SIAM and statistics venues

### Statistics

- theorem families: likelihood, sufficiency, minimax risk, asymptotics, nonparametric ideas
- applications: estimation, testing, causal inference, robust inference
- directions: high-dimensional inference, distribution-free inference, causal learning
- venue watch: JMLR, PMLR, statistics departments, high-dimensional statistics groups

### Real Analysis

- theorem families: convergence, continuity, compactness, function-space reasoning
- applications: rigorous optimization proofs, asymptotics, PDE and operator viewpoints
- directions: optimization theory, inverse problems, scientific computing
- venue watch: SIAM journals, applied math research groups

### Optimization

- theorem families: convexity, duality, KKT, first-order methods, variational arguments
- applications: ERM, constrained learning, inverse problems, robust control, online learning
- directions: optimization for ML, distributed optimization, robust and stochastic optimization
- venue watch: SIOPT, JMLR, ICML/PMLR, NeurIPS/OpenReview, SICON

### Numerical Methods

- theorem families: consistency, stability, conditioning, convergence, iterative methods
- applications: scalable solvers, approximation, scientific ML, inverse problems
- directions: randomized NLA, scientific computing, numerics for learning systems
- venue watch: SINUM, SIMAX, SISC, JMLR

### Matrix Analysis

- theorem families: PSD matrices, operator inequalities, perturbation bounds, matrix concentration
- applications: covariance estimation, kernel methods, graph learning, low-rank methods
- directions: random matrices, spectral learning, optimization geometry
- venue watch: SIMAX, COLT, JMLR, ICML/PMLR

### Learning Theory

- theorem families: PAC, VC, Rademacher complexity, stability, uniform convergence
- applications: generalization guarantees, regularization, sample complexity, algorithmic bias
- directions: deep learning theory, implicit bias, online learning, structure-aware generalization
- venue watch: COLT, ALT, JMLR, TMLR, ICML/PMLR

### High-Dimensional Probability

- theorem families: sub-Gaussian / sub-exponential tails, random matrices, chaining, concentration
- applications: covariance concentration, compressed sensing, sketching, matrix recovery
- directions: modern nonasymptotic theory, random features, high-dimensional geometry
- venue watch: COLT, JMLR, SIMAX, high-dimensional probability courses and workshops

### High-Dimensional Statistics

- theorem families: sparsity, minimax rates, regularized estimation, selective inference
- applications: genomics, multiple testing, large-scale inference, robust uncertainty
- directions: high-dimensional inference, causal structure learning, distribution-free methods
- venue watch: JMLR, PMLR, statistics research groups, workshops and seminars

## How A Single Topic Should Connect To Research

Each mature topic page should have a `Research Gateway` block near the bottom.

### Minimum required fields

1. `Why this topic matters in research`
2. `Main theorem family pages`
3. `One application page`
4. `Three-paper ladder`
5. `One active direction page`
6. `Venue watch`

### Example: SVD

On the `SVD` concept page, the research gateway could look like:

- theorem map: `spectral and low-rank methods`
- application page: `PCA, latent factors, and compression`
- paper ladder:
  - classic: low-rank approximation result
  - bridge: randomized linear algebra notes
  - current: a representative sketching or matrix approximation paper
- direction page: `randomized numerical linear algebra`
- venue watch: `SIMAX`, `ICML/PMLR`, `JMLR`

### Example: Concentration Inequalities

On the `Hoeffding / Bernstein / Matrix Bernstein` area, the gateway could link:

- theorem map: `concentration inequalities family`
- application page: `generalization and tail bounds`
- paper ladder:
  - classic: canonical concentration reference
  - bridge: course or survey notes
  - current: a modern high-dimensional or random-matrix paper
- direction page: `high-dimensional probability`
- venue watch: `COLT`, `JMLR`, `PMLR`, `SIMAX`

## Starter Research Pages To Build First

If you want the research layer to feel useful early, build these first:

1. `research/paper-labs/index.md`
2. `research/theorem-maps/index.md`
3. `research/applications/index.md`
4. `research/directions/index.md`
5. `foundations/linear-algebra/research/index.md`
6. `foundations/probability/research/index.md`
7. `foundations/optimization/research/index.md`
8. `foundations/linear-algebra/research/theorem-maps/spectral-and-low-rank-methods.md`
9. `foundations/probability/research/theorem-maps/concentration-inequalities-family.md`
10. `foundations/optimization/research/theorem-maps/convexity-and-duality-family.md`
11. `foundations/linear-algebra/research/applications/pca-and-low-rank-modeling.md`
12. `foundations/probability/research/applications/generalization-and-tail-bounds.md`
13. `foundations/optimization/research/applications/constrained-learning-and-regularization.md`
14. `foundations/linear-algebra/research/directions/randomized-numerical-linear-algebra.md`
15. `foundations/probability/research/directions/high-dimensional-probability.md`
16. `foundations/optimization/research/directions/optimization-for-machine-learning.md`

These pages create a visible research bridge early without forcing you to build every topic at once.

## Maintenance Policy

To keep the site trustworthy, treat different page classes differently.

### Stable core pages

- topic pages
- concept pages
- proof pages
- theorem family pages

Review roughly `yearly` or when the syllabus changes.

### Bridge pages

- survey pages
- application pages
- canonical paper labs

Review roughly `every 6 to 12 months`.

### Frontier pages

- research direction pages
- current paper labs
- venue pages

Review roughly `once per term` or `once per conference cycle`.

## Source Policy For The Research Layer

Use source types in this order:

1. `official course pages`
2. `author-maintained notes or books`
3. `official venue / journal pages`
4. `surveys and canonical papers`
5. `representative recent papers`

For current directions, keep a small venue watchlist instead of trying to maintain a giant live feed.

## Recommended Venue Watch Blocks

### Theory-heavy ML and learning

- `COLT`
- `ALT`
- `JMLR`
- `TMLR`
- `ICML / PMLR`
- `NeurIPS / OpenReview`

### Optimization, matrix methods, numerical analysis

- `SIAM Journal on Optimization`
- `SIAM Journal on Matrix Analysis and Applications`
- `SIAM Journal on Numerical Analysis`
- `ICML / PMLR`
- `JMLR`

### Control and dynamics

- `Learning for Dynamics and Control`
- `SIAM Journal on Control and Optimization`
- `IEEE Conference on Decision and Control`

## Why This Structure Fits Your Site

This system matches your broader website goal well because it supports all three major user intents:

1. `I want to build my math foundation`
2. `I want to understand one topic deeply`
3. `I want to read a theory-heavy paper and not get lost`

Most importantly, it makes every topic page answer:

- what the math is
- how it is proved
- where it is applied
- which papers use it
- what research direction grows out of it

That is exactly the right bridge from `basic -> advanced -> research`.

## Reference Signals

The overall design above is aligned with:

- Stanford's `paper-reading` structure, where introductory context comes before author-level discussion
- Keshav's `three-pass` reading method
- Levis's guidance on how to read research papers historically and conceptually
- ML theory venue ecosystems such as `COLT`, `JMLR`, `TMLR`, `PMLR`, and `OpenReview`
- applied-math venue ecosystems such as `SIOPT`, `SIMAX`, `SINUM`, and `SICON`
- current research-area pages in statistical learning, high-dimensional statistics, and control-oriented learning

Representative sources:

- [How to Read a Paper](https://web.stanford.edu/class/cs114/reading-keshav.pdf)
- [Reading a (CS or EE) Research Paper](https://stanford.edu/class/cs114/reading-levis.pdf)
- [Stanford CS114/214: Selected Readings of CS Research](https://web.stanford.edu/class/cs114/)
- [Association for Computational Learning / COLT](https://www.learningtheory.org/)
- [Transactions on Machine Learning Research](https://www.jmlr.org/tmlr/)
- [Proceedings of Machine Learning Research](https://proceedings.mlr.press/)
- [Journal of Machine Learning Research](https://jmlr.org/)
- [SIAM Journal on Optimization](https://www.siam.org/publications/siam-journals/siam-journal-on-optimization/)
- [SIAM Journal on Matrix Analysis and Applications](https://www.siam.org/publications/siam-journals/siam-journal-on-matrix-analysis-and-applications/)
- [SIAM Journal on Numerical Analysis](https://www.siam.org/publications/siam-journals/siam-journal-on-numerical-analysis/)
- [SIAM Journal on Control and Optimization](https://www.siam.org/publications/siam-journals/siam-journal-on-control-and-optimization/)
- [MIT 18.657 Mathematics of Machine Learning](https://www.ocw.mit.edu/courses/18-657-mathematics-of-machine-learning-fall-2015/)
- [Stanford Statistics: Statistical Learning](https://statistics.stanford.edu/research/statistical-learning)
- [Stanford Statistics: High-Dimensional Statistics](https://statistics.stanford.edu/research/high-dimensional-statistics)
- [Berkeley Statistics: High-Dimensional Data Analysis](https://statistics.berkeley.edu/research/high-dimensional-data-analysis)
- [Underactuated Robotics](https://underactuated.mit.edu/)
- [MIT 6.8210 Underactuated Robotics](https://underactuated.csail.mit.edu/Spring2024/)
- [Learning for Dynamics and Control](https://sites.google.com/usc.edu/l4dc2026/)
