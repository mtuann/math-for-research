# Content Production Map

## Purpose

This document turns the syllabus tree into a practical publishing plan.

The goal is not to write every page at once. The goal is to build the site in layers so that:

- the first public version already feels useful
- the strongest modules become reliable templates for the rest
- the highest-leverage topics get full `gold-standard` treatment

This plan assumes the contributor rules in:

- [CONTRIBUTING.md](CONTRIBUTING.md)
- [contributing/page-templates.md](contributing/page-templates.md)
- [authoring/research_page_templates.md](authoring/research_page_templates.md)

## Scope Snapshot

Current long-term scope from the syllabus tree:

- `17 core modules`
- `19 modules` with optional branches
- about `113` core topic pages before applications, paper labs, and research pages
- about `130` core pages if each module also has its own landing page

That means the right strategy is:

1. build a strong core spine
2. choose the first `40` topic pages very intentionally
3. promote only the best `15` topics into full multi-file packages

## Production Principles

Use these rules when choosing what to build next:

1. Prefer topics that unlock many later pages.
2. Prefer topics that connect `formal math -> computation -> application -> papers`.
3. Build modules that make the site distinctive for `CS / AI / engineering research`, not just broad for its own sake.
4. Delay lower-leverage branches until the main spine is trustworthy.
5. Treat `gold-standard` topics as reusable models for structure, tone, sourcing, and research bridges.

## Tier 1: Must-Build Modules

These are the first modules that should feel complete enough for public use.

### Tier 1A: Site Entry And Mathematical Language

Build these first because they reduce friction everywhere else:

- `Start Here`
- `Proofs`
- `Linear Algebra`
- `Probability`

Why these go first:

- `Start Here` teaches readers how to use the site and how to read theory
- `Proofs` teaches the language needed to survive rigorous pages later
- `Linear Algebra` is central for ML, optimization, numerics, signal, and matrix methods
- `Probability` is central for statistics, learning theory, concentration, and uncertainty

### Tier 1B: Bridge To Research-Ready Math

Build these next because they connect the foundation to real research workflows:

- `Multivariable Calculus`
- `Statistics`
- `Optimization`
- `Real Analysis`

Why these come next:

- `Multivariable Calculus` unlocks gradients, Jacobians, Hessians, and constrained optimization
- `Statistics` turns probability into inference and experiment interpretation
- `Optimization` is the language of objectives, constraints, certificates, and training
- `Real Analysis` upgrades the reader from computational fluency to proof-level control of convergence

### Tier 1C: Delay Until The Core Spine Is Stable

Do not ignore these, but do not let them slow the first serious release:

- `Algebra Repair`
- `Logic`
- `Discrete Math`
- `Single-Variable Calculus`
- `ODEs`
- `Numerical Methods`
- `Matrix Analysis`
- `Learning Theory`
- `High-Dimensional Probability`
- `High-Dimensional Statistics`
- `Information Theory`
- `Control`

These matter a lot, but they should mostly come after the site has a strong public backbone.

## Tier 2: First 40 Topic Pages

These are the first `40` core topic pages to build. Together they create a strong site identity and a usable dependency chain.

### A. Proofs (`6`)

1. `statements-and-quantifiers`
2. `direct-proof`
3. `contrapositive-and-contradiction`
4. `induction`
5. `counterexamples-and-proof-debugging`
6. `proof-writing-clinic`

### B. Linear Algebra (`6`)

7. `vectors-and-linear-combinations`
8. `matrices-and-linear-maps`
9. `subspaces-basis-dimension`
10. `orthogonality-and-least-squares`
11. `eigenvalues-eigenvectors-diagonalization`
12. `svd-and-low-rank-approximation`

### C. Probability (`6`)

13. `sample-spaces-events-conditioning`
14. `random-variables-and-distributions`
15. `expectation-variance-covariance`
16. `joint-conditional-and-bayes`
17. `law-of-large-numbers-and-clt`
18. `concentration-and-common-inequalities`

### D. Multivariable Calculus (`6`)

19. `partial-derivatives-and-gradients`
20. `jacobians-and-hessians`
21. `chain-rule-and-linearization`
22. `multiple-integrals`
23. `constrained-optimization`
24. `vector-fields-and-divergence-curl`

### E. Statistics (`6`)

25. `descriptive-statistics-and-data-models`
26. `estimation-and-bias-variance`
27. `maximum-likelihood-and-bayesian-basics`
28. `confidence-intervals-and-hypothesis-testing`
29. `regression-and-classification-basics`
30. `experimental-design-and-model-evaluation`

### F. Optimization (`5`)

31. `convex-sets-and-separation`
32. `convex-functions-and-subgradients`
33. `unconstrained-first-order-methods`
34. `constrained-optimization-kkt-and-lagrangians`
35. `duality-and-certificates`

### G. Real Analysis (`5`)

36. `rigorous-convergence`
37. `continuity-compactness-completeness`
38. `sequences-and-series-of-functions`
39. `differentiation-and-integration-as-theorems`
40. `fixed-point-implicit-and-inverse-function-ideas`

## Why These 40

This set is the best first production target because it gives the site:

- a proof language
- the main linear algebra and probability spine for ML and engineering
- the calculus-to-optimization bridge
- the statistics layer needed for experiments and inference
- the analysis layer needed for serious theorem reading

It also creates a strong path for later advanced modules:

`proofs -> linear algebra -> probability -> multivariable calculus -> statistics -> optimization -> real analysis`

## Tier 3: First 15 Gold-Standard Topics

These are the first topics that should be promoted beyond a single concept page into a full package with:

- concept page
- proof page
- exercise page
- application page
- paper-lab page
- research-direction page
- source guide

### Proof And Math Language

1. `statements-and-quantifiers`
2. `induction`

### Linear Algebra

3. `orthogonality-and-least-squares`
4. `eigenvalues-eigenvectors-diagonalization`
5. `svd-and-low-rank-approximation`

### Multivariable Calculus

6. `partial-derivatives-and-gradients`
7. `jacobians-and-hessians`

### Probability And Statistics

8. `random-variables-and-distributions`
9. `expectation-variance-covariance`
10. `joint-conditional-and-bayes`
11. `law-of-large-numbers-and-clt`
12. `concentration-and-common-inequalities`
13. `maximum-likelihood-and-bayesian-basics`
14. `regression-and-classification-basics`

### Optimization

15. `constrained-optimization-kkt-and-lagrangians`

## Why These 15 Become Gold Standard

These topics do the best job of showing the full identity of the site:

- they are mathematically central
- they connect clearly to AI, ML, statistics, optimization, or engineering
- they support theorem pages, worked examples, and applications naturally
- they make it easy to build `paper bridges`
- they give future contributors a clear standard to imitate

## What To Delay Until Later

Do not spend early energy on these unless they are directly needed for a near-term publishing goal:

- optional branches like `information theory` and `control`
- very specialized frontier pages before the foundational page is strong
- large bibliography-heavy `library` pages before topic pages have real substance
- top-level publication pages beyond the current starter set
- low-value breadth pages that duplicate textbook tables of contents without explanation

## Best First Gold-Standard Example

The best first `gold-standard` topic to build is:

`orthogonality-and-least-squares`

## Why This Should Go First

This topic is the strongest template topic because it has all the right ingredients at once:

- it is foundational, but not trivial
- it has clean geometric intuition
- it has a natural theorem and proof story
- it has a strong computation story
- it connects immediately to regression, approximation, and inverse problems
- it naturally bridges to PCA, SVD, optimization, and numerical methods
- it appears constantly in real papers, but is still teachable without too much machinery

It is easier to turn into a complete package than `SVD`, while still giving you a very research-relevant result.

## Recommended Gold-Standard Package For `orthogonality-and-least-squares`

Use this file set:

1. `concepts/orthogonality-and-least-squares.qmd`
2. `proofs/projection-theorem-and-normal-equations.qmd`
3. `exercises/orthogonality-and-least-squares.qmd`
4. `applications/linear-regression-through-projection.qmd`
5. `paper-lab/from-least-squares-to-modern-regression.qmd`
6. `research/least-squares-sketching-and-overparameterized-regimes.qmd`
7. `sources/orthogonality-and-least-squares.qmd`

## What This Example Should Demonstrate

This first gold-standard topic should become the model for the whole site.

It should demonstrate:

- how to open with intuition without being vague
- how to transition into formal statements cleanly
- how to teach a proof without becoming opaque
- how to connect math to one practical mechanism
- how to connect a foundation topic to current papers without overselling novelty
- how to annotate resources as `First pass`, `Second pass`, and `Paper bridge`
- how to separate stable core from active frontier

## Second And Third Gold-Standard Candidates

After `orthogonality-and-least-squares`, the next best topics to promote are:

1. `svd-and-low-rank-approximation`
2. `concentration-and-common-inequalities`

These work well because:

- `SVD` gives the site an iconic linear algebra and representation-learning bridge
- `Concentration` gives the site a strong doorway into modern theory papers

## Recommended Publishing Order After The First Gold Standard

1. Finish the full `orthogonality-and-least-squares` package
2. Promote `svd-and-low-rank-approximation`
3. Promote `concentration-and-common-inequalities`
4. Promote `constrained-optimization-kkt-and-lagrangians`
5. Promote `maximum-likelihood-and-bayesian-basics`

That sequence gives the site a strong shape across:

- geometry
- probability
- optimization
- inference
- paper reading

## Practical Rule Of Thumb

For the first public release:

- make `7 to 8 modules` feel trustworthy
- make `40` topic pages exist and read well
- make `3 to 5` gold-standard topics so good that every future contributor can copy their structure

That is enough to make the site feel serious without needing to finish the entire syllabus tree first.
