# Website Syllabus Tree

## Goal

Design a public `GitHub Pages` website that helps a learner:

- build math from `basic -> advanced`
- understand one topic clearly on a single page
- see `why it matters`
- connect theory to `applications, algorithms, and systems`
- bridge into `papers, surveys, and research directions`

The site should feel like:

- a `modern math textbook`
- a `research map`
- a `paper-reading companion`
- a `long-term knowledge base`

It should **not** be themed around any one school, book collection, or syllabus.

Local books, UIUC, MIT, Stanford, blogs, notes, and papers are all `references inside the site`, not the site’s identity.

## Recommended Stack

Use:

- `Quarto`
- `GitHub Actions`
- `GitHub Pages`

Why this is the best fit:

- Quarto has strong built-in support for `LaTeX math`
- Quarto supports `equation`, `theorem`, `proof`, `figure`, and `section` cross-references
- Quarto works well for `websites`, `blogs`, and `book-like` content
- GitHub officially supports deploying static generators through `custom workflows`
- this stack is better for a math-heavy site than default Jekyll, and lighter than forcing the whole site into a React docs app

Recommended math rendering:

- `MathJax` first
- `KaTeX` later only if you want faster render and can live with a smaller feature set

## Core Site Model

Build the site as one `Quarto website project` first.

Inside that website, organize content into:

1. `Start Here`
2. `Roadmaps`
3. `Foundation`
4. `Advanced`
5. `Applications`
6. `Paper Lab`
7. `Research`
8. `Publication`
9. `Library`
10. `Essays / Notes`

Later, if one major section becomes large enough, it can be split into a Quarto `book`.

## Top-Level Navigation

Recommended top navigation:

- `Home`
- `Start Here`
- `Roadmaps`
- `Topics`
- `Applications`
- `Paper Lab`
- `Research`
- `Publication`
- `Library`
- `Notes`

Recommended sidebar pattern:

- left sidebar by `topic tree`
- right sidebar for `on-page structure`

## Site Identity

The site’s main identity should be:

`Math for CS / AI / Engineering Research`

Possible subtitle:

`From foundations to theory-heavy papers`

## Global Learning Loop

Every serious topic should follow the same loop:

`Learn -> Prove -> Solve -> Apply -> Read`

That means each topic should eventually include:

- concept explanation
- formal statements
- proof patterns
- worked examples
- exercises
- application bridges
- paper-reading bridges

## Global Information Architecture

```text
/ 
  home
  start-here
  roadmaps
  topics
  applications
  paper-lab
  research
  publication
  library
  notes
```

## Recommended Quarto Project Shape

```text
math4life/
  _quarto.yml
  index.qmd
  about.qmd
  styles.scss
  references.bib
  CNAME

  start-here/
    index.qmd
    how-to-use-this-site.qmd
    math-diagnostic.qmd
    notation-and-symbols.qmd
    how-to-write-proofs.qmd
    how-to-read-theory-papers.qmd

  roadmaps/
    index.qmd
    core-foundation.qmd
    theory-reading.qmd
    ai-ml-theory.qmd
    engineering-systems.qmd

  topics/
    foundation/
      algebra-repair/
      proofs/
      logic/
      discrete-math/
      single-variable-calculus/
      linear-algebra/
      multivariable-calculus/
      odes/
      probability/
      statistics/

    advanced/
      real-analysis/
      optimization/
      numerical-methods/
      matrix-analysis/
      learning-theory/
      high-dimensional-probability/
      high-dimensional-statistics/
      information-theory/
      control/

  applications/
    index.qmd
    machine-learning.qmd
    optimization-and-inference.qmd
    scientific-computing.qmd
    control-and-dynamics.qmd
    signal-and-communication.qmd

  paper-lab/
    index.qmd
    how-to-read-a-paper.qmd
    theorem-decoder.qmd
    notation-translation.qmd
    dependency-maps.qmd
    reading-trails/

  research/
    index.qmd
    theorem-families/
    directions/
    surveys/
    venues/

  publication/
    index.qmd
    how-top-venue-papers-are-shaped.qmd
    venue-map.qmd
    claim-evidence-matrix.qmd
    theorem-to-experiment-alignment.qmd
    writing-theory-sections.qmd
    writing-experiment-sections.qmd
    related-work-and-positioning.qmd
    reproducibility-checklist.qmd
    review-and-rebuttal.qmd

  library/
    index.qmd
    books.qmd
    courses.qmd
    notes.qmd
    papers.qmd

  notes/
    index.qmd
    posts/
```

## Topic Folder Pattern

Every mature topic folder should have the same internal structure:

```text
topic-name/
  index.qmd
  concepts/
  proofs/
  exercises/
  applications/
  paper-lab/
  research/
  sources/
```

This is for `topic learning`.

Publication guidance should stay mostly in a separate top-level `publication/` section, with only lightweight links back from advanced modules and paper labs.

Example:

```text
topics/foundation/linear-algebra/
  index.qmd
  concepts/
    vectors-and-linear-combinations.qmd
    matrices-and-linear-maps.qmd
    subspaces-basis-dimension.qmd
    orthogonality-and-least-squares.qmd
    eigenvalues-eigenvectors-diagonalization.qmd
    svd-and-low-rank-approximation.qmd
  proofs/
    rank-nullity.qmd
    spectral-theorem-intuition.qmd
    least-squares-normal-equations.qmd
  exercises/
    warmup.qmd
    core.qmd
    proof-based.qmd
    computational.qmd
  applications/
    pca-and-dimensionality-reduction.qmd
    least-squares-and-regression.qmd
    spectral-methods-in-graphs.qmd
  paper-lab/
    reading-guide.qmd
    classic-paper.qmd
    modern-paper.qmd
  research/
    theorem-family.qmd
    current-directions.qmd
  sources/
    source-guide.qmd
```

## Main Syllabus Tree

### Start Here

```text
/start-here
  /how-to-use-this-site
  /math-diagnostic
  /notation-and-symbols
  /how-to-write-proofs
  /how-to-read-theory-papers
```

### Foundation Track

```text
/topics/foundation
  /algebra-repair
    /expressions-equations-inequalities
    /functions-and-graphs
    /exponents-logarithms
    /trigonometry-and-complex-numbers
    /symbol-manipulation-lab

  /proofs
    /statements-and-quantifiers
    /direct-proof
    /contrapositive-and-contradiction
    /induction
    /counterexamples-and-proof-debugging
    /proof-writing-clinic

  /logic
    /propositional-logic
    /predicate-logic
    /sets-functions-relations
    /logical-equivalence-and-negation
    /translation-between-english-and-symbols

  /discrete-math
    /counting-and-combinatorics
    /recurrences-and-asymptotics
    /graphs-and-trees
    /basic-number-theory
    /discrete-probability-preview

  /single-variable-calculus
    /limits-and-continuity
    /derivatives-and-optimization
    /integrals-and-accumulation
    /series-and-taylor-expansions
    /approximation-and-modeling

  /linear-algebra
    /vectors-and-linear-combinations
    /matrices-and-linear-maps
    /subspaces-basis-dimension
    /orthogonality-and-least-squares
    /eigenvalues-eigenvectors-diagonalization
    /svd-and-low-rank-approximation

  /multivariable-calculus
    /partial-derivatives-and-gradients
    /jacobians-and-hessians
    /chain-rule-and-linearization
    /multiple-integrals
    /constrained-optimization
    /vector-fields-and-divergence-curl

  /odes
    /first-order-odes
    /second-order-linear-odes
    /systems-of-odes
    /matrix-exponential
    /stability-and-phase-portraits
    /modeling-dynamical-systems

  /probability
    /sample-spaces-events-conditioning
    /random-variables-and-distributions
    /expectation-variance-covariance
    /joint-conditional-and-bayes
    /law-of-large-numbers-and-clt
    /concentration-and-common-inequalities

  /statistics
    /descriptive-statistics-and-data-models
    /estimation-and-bias-variance
    /maximum-likelihood-and-bayesian-basics
    /confidence-intervals-and-hypothesis-testing
    /regression-and-classification-basics
    /experimental-design-and-model-evaluation
```

### Advanced Track

```text
/topics/advanced
  /real-analysis
    /rigorous-convergence
    /continuity-compactness-completeness
    /sequences-and-series-of-functions
    /differentiation-and-integration-as-theorems
    /fixed-point-implicit-and-inverse-function-ideas
    /applications-in-optimization-probability-and-learning
    /paper-bridge

  /optimization
    /convex-sets-and-separation
    /convex-functions-and-subgradients
    /unconstrained-first-order-methods
    /constrained-optimization-kkt-and-lagrangians
    /duality-and-certificates
    /stochastic-and-proximal-methods
    /nonconvex-landscape-intuition
    /applications-in-ml-signal-and-control
    /paper-bridge

  /numerical-methods
    /floating-point-conditioning-and-stability
    /direct-linear-solvers-and-factorizations
    /iterative-methods-and-preconditioning
    /eigenvalue-and-svd-computation
    /interpolation-approximation-and-quadrature
    /nonlinear-equations-and-optimization-solvers
    /randomized-and-large-scale-numerics
    /applications-in-scientific-ml-and-engineering
    /paper-bridge

  /matrix-analysis
    /norms-singular-values-and-operator-viewpoints
    /psd-matrices-loewner-order-and-quadratic-forms
    /spectral-theorems-and-functional-calculus
    /perturbation-interlacing-and-stability
    /trace-determinant-and-matrix-inequalities
    /low-rank-kernel-and-geometry-links
    /applications-in-optimization-learning-and-random-matrices
    /paper-bridge

  /learning-theory
    /erm-and-uniform-convergence
    /pac-vc-and-sample-complexity
    /rademacher-stability-and-generalization
    /surrogate-losses-regularization-and-margin
    /online-learning-and-optimization-links
    /modern-generalization-double-descent-and-implicit-bias
    /applications-in-classification-representation-and-foundation-models
    /paper-bridge

  /high-dimensional-probability
    /concentration-of-measure
    /subgaussian-subexponential-and-psi-norms
    /random-vectors-covering-and-geometry
    /random-matrices-and-spectral-concentration
    /chaining-symmetrization-and-empirical-process-flavor
    /dimension-reduction-and-embedding-results
    /applications-in-ml-statistics-and-signal-processing
    /paper-bridge

  /high-dimensional-statistics
    /sparsity-regularization-and-structural-assumptions
    /lasso-compressed-sensing-and-convex-recovery
    /estimation-rates-minimax-and-non-asymptotic-bounds
    /inference-after-selection-and-debiasing
    /low-rank-graphical-and-latent-structure-models
    /robust-and-distribution-shift-aware-estimation
    /applications-in-causal-bio-and-modern-ml
    /paper-bridge

  /information-theory
    /entropy-mutual-information-and-kl
    /coding-channel-capacity-and-converse-proofs
    /rate-distortion-and-representation
    /information-theoretic-lower-bounds
    /applications-in-ml-language-and-communication
    /paper-bridge

  /control
    /linear-systems-stability-and-state-space
    /controllability-observability-and-realization
    /optimal-control-and-dynamic-programming
    /stochastic-control-and-mdp-bridges
    /robust-nonlinear-and-learning-based-control
    /applications-in-robotics-rl-and-systems
    /paper-bridge
```

## Dependency Flow

The site should make dependencies visible.

Main dependencies:

- `Algebra -> Calculus -> Multivariable Calculus -> ODEs`
- `Algebra -> Proofs -> Logic -> Discrete Math`
- `Single-Variable Calculus + Linear Algebra -> Multivariable Calculus`
- `Proofs + Discrete Math + Calculus -> Probability -> Statistics`
- `Probability + Statistics + Calculus + Linear Algebra -> Learning Theory`
- `Proofs + Calculus + Linear Algebra -> Real Analysis -> Optimization / High-Dimensional Probability`
- `Linear Algebra + Optimization + Numerics -> Matrix Analysis`
- `High-Dimensional Probability + Statistics + Optimization -> High-Dimensional Statistics`

Important sequencing rule:

- start `Linear Algebra` early
- do not wait until all calculus is “finished”
- keep `Probability before Statistics`
- treat `Real Analysis` as the upgrade from “computational comfort” to “proof maturity”

## Page Types

Every mature topic should use a consistent page system.

### 1. Module Overview

Use this as the landing page for a module.

It should contain:

- what the module is
- why it matters
- prerequisites
- dependency map
- learning outcomes
- module order
- application areas
- paper-reading relevance
- source shelf

### 2. Topic Page

This is the main teaching page.

It should contain:

- `Role`
  One sentence on what this topic is for.
- `Why It Matters`
  Where it shows up in CS, AI, engineering, optimization, statistics, control, or learning.
- `Prerequisites`
  What the reader should know before reading.
- `Intuition`
  The idea before the formalism.
- `Formal Core`
  Definitions, notation, key statements.
- `Main Results`
  Theorems, lemmas, identities, or algorithmic claims.
- `Proof Patterns`
  How people usually prove things in this area.
- `Worked Example`
  A concrete example done carefully.
- `Computation Lens`
  What this means in code, simulation, or numerical work.
- `Application Lens`
  Real use in models, algorithms, or systems.
- `Paper Bridge`
  2 to 5 papers or notes with reading guidance.
- `Common Mistakes`
  Misreadings, notation traps, wrong intuitions.
- `Exercises`
  Warm-up, core, proof-based, computational.
- `Next Topics`
  What this unlocks next.

### 3. Theorem Page

Use when one theorem family deserves its own page.

It should contain:

- theorem statement
- assumptions
- why assumptions matter
- dependency tree
- proof sketch
- proof variants
- where this theorem appears in papers
- applications

### 4. Proof Clinic

Use for proof-writing skill.

It should contain:

- proof strategy pattern
- annotated proof
- common failure modes
- fill-in-the-gap version
- rewrite checklist

### 5. Application Page

Use for concrete use-cases.

It should contain:

- problem setup
- which math tools are used
- how the math changes the algorithm or analysis
- minimal implementation idea
- model limitations
- related papers

### 6. Paper Lab

Use for theory-heavy reading.

It should contain:

- why this paper matters
- prerequisites
- notation map
- theorem dependency map
- first pass summary
- second pass proof map
- application takeaway
- what to read next

### 7. Research Direction Page

Use for frontier overview.

It should contain:

- stable core math behind the direction
- active questions
- representative papers
- typical venues
- what background is required
- how this direction connects to other topics

### 8. Source Guide

Use for references.

It should contain:

- primary sources
- first-pass resources
- second-pass resources
- problem sources
- surveys and notes
- how to use the references

## Topic Page Anatomy

If you want each single topic page to feel complete and clear, use this exact sequence:

1. `One-line role`
2. `Problem that motivates it`
3. `Core intuition`
4. `Formal definitions`
5. `Canonical example`
6. `Main theorem or identity`
7. `Why the theorem matters`
8. `Proof sketch or proof pattern`
9. `Computation or algorithmic interpretation`
10. `Application examples`
11. `Paper bridge`
12. `Exercises`
13. `Common mistakes`
14. `Where to go next`

This order works because it moves from `motivation -> formalism -> use`.

## Research Integration Layer

Research should be embedded, not isolated.

Every major topic folder should have:

```text
research/
  index.qmd
  theorem-maps/
  applications/
  paper-labs/
  directions/
```

Top-level research should then aggregate these:

```text
research/
  theorem-families/
  directions/
  surveys/
  venues/
  reading-trails/
```

Research page categories:

- `theorem family`
- `application bridge`
- `paper lab`
- `direction page`
- `survey trail`

## Publication Layer

Yes, the site should include publication guidance, but it should be framed as:

- `how strong research papers are built`
- `how theory, experiments, and claims fit together`
- `how different venue cultures evaluate work`

It should **not** become:

- a promise machine for “getting into top venues”
- a prestige-first layer that overwhelms the math
- a substitute for actually learning the material

Best design rule:

`Publication is an advanced workflow layer built on top of the math and paper-reading system.`

That keeps the site serious and useful.

## Publication Section Tree

```text
/publication
  /how-top-venue-papers-are-shaped
  /venue-map
  /claim-evidence-matrix
  /theorem-to-experiment-alignment
  /writing-theory-sections
  /writing-experiment-sections
  /related-work-and-positioning
  /reproducibility-checklist
  /review-and-rebuttal
```

## What The Publication Section Should Teach

### 1. How Top-Venue Papers Are Shaped

Teach:

- what makes a paper feel `conference-ready` or `journal-ready`
- how strong papers align `problem -> method -> theorem -> experiment -> claim`
- how papers differ across theory-heavy and empirical venues

This page should emphasize:

- clarity
- contribution type
- evidence quality
- positioning

not prestige language.

### 2. Venue Map

Teach:

- how venue culture differs by field
- which venues are theory-heavy vs empirical vs systems vs journals
- how to think about fit, not just rank

Example venue groups the page can discuss:

- `ML / AI theory`: `COLT`, `JMLR`, `TMLR`, theory tracks at `NeurIPS`, `ICML`, `ICLR`
- `optimization`: `SIOPT`
- `matrix / numerical analysis`: `SIMAX`, `SINUM`
- `control`: `SICON`, `CDC`

The goal is:

- `understand review culture`
- `understand expected evidence`
- `understand where different kinds of contributions belong`

### 3. Claim-Evidence Matrix

This should be one of the most important pages in the entire publication layer.

Teach:

- every major claim must have matching evidence
- theorems need assumptions, scope, and interpretation
- experiments need ablations, baselines, and failure cases
- system claims need scale, efficiency, and reproducibility support

Useful page structure:

- claim type
- required evidence
- common weak evidence
- reviewer objections

### 4. Theorem-to-Experiment Alignment

Teach:

- how theoretical claims should influence experiment design
- which empirical tests actually support a theorem-informed story
- how to avoid disconnected “theory section” and “experiment section” writing

This is especially useful for your audience.

### 5. Writing Theory Sections

Teach:

- how to present assumptions
- how to motivate the theorem
- how to state the main result cleanly
- how much proof detail belongs in the main paper vs appendix
- how to explain significance, not just derivation

### 6. Writing Experiment Sections

Teach:

- benchmark choice
- baseline choice
- ablation design
- robustness and sensitivity checks
- reproducibility expectations
- what makes results tables persuasive

### 7. Related Work and Positioning

Teach:

- how to position a contribution honestly
- how to separate `similar`, `closest`, and `different` work
- how to build a related-work section that helps rather than name-drops

### 8. Reproducibility Checklist

Teach:

- code release expectations
- seed control
- hyperparameter disclosure
- data availability
- compute reporting
- theorem appendix and proof completeness

### 9. Review and Rebuttal

Teach:

- how reviewers usually attack weak claims
- how to interpret reviews
- how to respond without becoming defensive
- how to turn reviews into a revision plan

## Publication Page Templates

Use three main templates here.

### Publication Guide Page

For pages like `writing-theory-sections` or `related-work-and-positioning`.

Include:

- objective
- why reviewers care
- strong pattern
- weak pattern
- examples
- checklist

### Venue Guide Page

For the `venue-map` and later venue-specific pages.

Include:

- venue type
- what kinds of contributions fit
- what evidence is usually expected
- what usually gets criticized
- related topics on the site

### Review Workflow Page

For rebuttal and revision pages.

Include:

- common reviewer concerns
- diagnosis questions
- revision actions
- what to change in theorem/experiment/writing

## How Publication Connects To The Rest Of The Site

Connections should look like this:

- `topic page -> application page -> paper lab -> publication guide`
- `learning theory / optimization / statistics / matrix analysis -> theorem-to-experiment alignment`
- `paper lab -> claim-evidence matrix`
- `research direction page -> venue map`

This way publication guidance grows naturally out of:

- understanding the math
- reading the literature
- learning how strong papers are assembled

## Placement In The Build Order

Do not publish the full publication layer first.

Recommended timing:

- publish `Claim-Evidence Matrix` early
- publish `How Top-Venue Papers Are Shaped` once you have `Paper Lab`
- publish `Writing Theory Sections` and `Theorem-to-Experiment Alignment` when the advanced modules are live
- publish `Venue Map` and `Review/Rebuttal` later

This keeps the site grounded in substance.

## Applications Section

Keep applications as a first-class top-level section.

Recommended application hubs:

- `Machine Learning`
- `Optimization and Inference`
- `Scientific Computing`
- `Signal and Communication`
- `Control and Dynamical Systems`
- `Graphs, Networks, and Algorithms`

Each application hub should link back to topic pages.

Example:

- `PCA` links back to `SVD`, `least squares`, `covariance`, `spectral theory`
- `Gradient descent in deep learning` links back to `multivariable calculus`, `optimization`, `conditioning`
- `Kalman filtering` links back to `linear systems`, `probability`, `Gaussian conditioning`

## Paper Lab Section

This should be one of the strongest parts of the site.

Recommended pages:

- `How to Read a Theory Paper`
- `How to Decode Notation`
- `How to Trace a Theorem Dependency Graph`
- `How to Read Assumptions`
- `How to Connect a Proof to an Experiment`
- `Reading Trails by Topic`

Reading trails should be organized as:

- `classic`
- `bridge`
- `modern`

Example:

- `Convex optimization trail`
- `Learning theory trail`
- `Random matrices trail`
- `Control and RL trail`

## Library Section

The library should be a reference hub, not the main structure.

Recommended groupings:

- by `topic`
- by `level`
- by `resource type`
- by `use case`

Resource types:

- books
- course pages
- lecture notes
- surveys
- papers
- blogs

Each library page should explain:

- what it is best for
- who it is for
- when to use it
- whether it is first pass, second pass, or paper support

## Suggested Front Matter

Every serious content page should have structured metadata.

Suggested fields:

```yaml
title:
slug:
section:
module:
level:
status:
prerequisites:
outcomes:
applications:
papers:
surveys:
tags:
keywords:
difficulty:
last_reviewed:
next:
```

Useful optional fields:

```yaml
theorems:
proof_patterns:
computational_tools:
venues:
research_directions:
```

## Suggested URL Pattern

- module overview: `/topics/<track>/<module>/`
- concept page: `/topics/<track>/<module>/concepts/<slug>/`
- proof page: `/topics/<track>/<module>/proofs/<slug>/`
- application page: `/topics/<track>/<module>/applications/<slug>/`
- paper lab page: `/topics/<track>/<module>/paper-lab/<slug>/`
- research page: `/topics/<track>/<module>/research/<slug>/`
- top-level application page: `/applications/<slug>/`
- top-level research page: `/research/<slug>/`

## Homepage Structure

Recommended homepage blocks:

1. Hero
2. Start paths
3. Main roadmap
4. Featured topics
5. Featured applications
6. Featured paper labs
7. Featured research directions
8. Recent notes

Three main start paths:

- `I want to build foundations`
- `I want to understand a topic`
- `I want to read a hard paper`

## Publishing Strategy

Build the site in layers.

### Layer 1

Publish:

- home
- start-here
- roadmap
- proofs
- linear algebra
- probability

### Layer 2

Publish:

- multivariable calculus
- optimization
- statistics
- paper-lab starter pages

### Layer 3

Publish:

- real analysis
- numerical methods
- matrix analysis
- applications section
- claim-evidence matrix

### Layer 4

Publish:

- learning theory
- high-dimensional probability
- high-dimensional statistics
- research directions
- publication layer

## First 20 Pages To Publish

1. `Home`
2. `How to Use This Site`
3. `Math Diagnostic`
4. `How to Write Proofs`
5. `How to Read Theory Papers`
6. `Core Foundation Roadmap`
7. `Linear Algebra Module Overview`
8. `Vectors and Linear Combinations`
9. `Orthogonality and Least Squares`
10. `SVD and Low-Rank Approximation`
11. `Probability Module Overview`
12. `Random Variables and Distributions`
13. `Expectation, Variance, Covariance`
14. `Concentration and Common Inequalities`
15. `Optimization Module Overview`
16. `Convex Functions and Subgradients`
17. `Gradient Methods`
18. `PCA Application Page`
19. `How to Decode a Theorem`
20. `Learning Theory Roadmap`

## Best First Publication Pages

If you add publication guidance, start with these:

1. `Claim-Evidence Matrix`
2. `How Top-Venue Papers Are Shaped`
3. `Theorem-to-Experiment Alignment`
4. `Writing Theory Sections`
5. `Related Work and Positioning`

## Main Recommendation

The best version of this site is not a list of resources.

It is a `structured math system` where:

- each topic is explained clearly
- the proofs are readable
- the applications are visible
- the papers are guided
- the publication workflow is demystified
- the research directions are connected

That is what will make it genuinely valuable and worth publishing.

## Sources

- [GitHub Pages custom workflows](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages)
- [GitHub Pages publishing source guidance](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [Creating a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)
- [Quarto creating a website](https://quarto.org/docs/websites/)
- [Quarto GitHub Pages publishing](https://quarto.org/docs/publishing/github-pages.html)
- [Quarto HTML math support](https://quarto.org/docs/output-formats/html-basics.html)
- [Quarto cross references](https://quarto.org/docs/authoring/cross-references.html)
- [Quarto book crossrefs](https://quarto.org/docs/books/book-crossrefs.html)
- [Docusaurus math equations](https://docusaurus.io/docs/markdown-features/math-equations)
- [Docusaurus deployment](https://docusaurus.io/docs/deployment)
- [Material for MkDocs math](https://squidfunk.github.io/mkdocs-material/reference/math/)
