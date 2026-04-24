# Math Foundation Website Plan

## Goal

Build a research-first math website for a future PhD in `CS / AI / engineering`.

The site should help with three things at the same time:

1. Build foundations from weak or uneven prerequisites.
2. Progress from computational comfort to proof-level understanding.
3. Read theory-heavy papers without getting blocked by notation, hidden assumptions, or missing lemmas.

## Main Insight

Your local library is already strong for the `intermediate -> advanced -> research` half of the journey:

- `Convex Optimization.pdf`
- `Introductory Lectures on Convex Optimization.pdf`
- `Matrix Analysis.pdf`
- `Numerical linear algebra.pdf`
- `Foundations_of_Machine_Learning.pdf`
- `Understanding Machine Learning From Theory to Algorithms.pdf`
- `The Elements of Statistical Learning.pdf`
- `High-Dimensional Probability.pdf`
- `High-Dimensional Statistics-short.pdf`
- `High-Dimensional Statistics.pdf`
- `dm.pdf` (`Algorithms for Decision Making`)

You also already have a strong seed document in:

- `/Users/mitu/Desktop/data/math/books/math-for-beginner/math.tex`

But the visible corpus is not yet a full `true beginner -> advanced` ladder. The main missing layer is:

- proof writing and discrete foundations
- beginner linear algebra
- single-variable and multivariable calculus as a guided sequence
- first-course probability and statistics
- first rigorous real analysis
- broad engineering foundations like ODE/PDE/control if you want more than ML theory

So the website should not present your current shelf as if it were already beginner-complete. It should explicitly bridge into your stronger books.

## Site Strategy

Design the site around three entry modes:

1. `Follow a roadmap`
2. `Look up a topic`
3. `Unpack a paper`

That gives you one site for both long-horizon study and urgent research needs.

Use one learning loop everywhere:

`Learn -> Prove -> Solve -> Read -> Build`

This prevents the site from becoming only a reading list or only a note dump.

## Recommended Information Architecture

### 1. Home

Purpose:

- explain who the site is for
- show the progression from basics to research math
- give three entry buttons: `Start Here`, `Roadmaps`, `Paper Lab`

Hero promise:

- "Build the math needed for AI, ML, CS, and engineering research, from foundations to paper reading."

### 2. Start Here

Purpose:

- placement diagnostic
- prerequisite map
- notation guide
- study method guide
- "how to learn math as a researcher"

Core pages:

- `Who This Site Is For`
- `Placement Check`
- `Notation and Symbols`
- `How to Study Proofs`
- `How to Read Theory Papers`

### 3. Roadmaps

Purpose:

- give clean top-down learning tracks

Recommended roadmap pages:

- `Core Math Foundation`
- `AI / ML Theory Track`
- `Engineering Systems Track`
- `Paper-Reading Track`
- `Federated Learning / Low-Rank Specialization` later

### 4. Foundations

This is the main teaching area.

Recommended order:

1. `Proofs and Mathematical Thinking`
2. `Discrete Math and Logic`
3. `Single-Variable Calculus`
4. `Linear Algebra`
5. `Multivariable Calculus`
6. `Probability`
7. `Statistics`
8. `Optimization`
9. `Numerical Linear Algebra and Numerical Methods`
10. `Real Analysis`
11. `Matrix Analysis`
12. `High-Dimensional Probability and Statistics`

### 5. Paper Lab

Purpose:

- convert textbook knowledge into paper-reading skill

Recommended pages:

- `Three-Pass Reading Method`
- `How to Decode a Theorem`
- `Assumptions Checklist`
- `Notation Translation`
- `Dependency Map`
- `Reproduce the Proof Skeleton`
- `Reproduce the Experiment`

### 6. Practice

Purpose:

- central place for exercises and labs

Recommended sections:

- `Proof Drills`
- `Computation Drills`
- `Exercise Ladders`
- `Mini Capstones`
- `Theory-to-Code Labs`

### 7. Library

Purpose:

- organize books and papers by level and use-case

Views:

- by topic
- by level
- by research use
- by local ownership

Recommended metadata on each source page:

- level
- prerequisites
- best use
- strongest chapters
- what to skip on first pass
- which roadmap modules use it

### 8. Research Workflow

Purpose:

- keep your existing `math.tex` strengths, but move them out of the beginner path

Recommended pages:

- `How to Build a Theory Section`
- `How to Keep a Reading Tracker`
- `Claim -> Theorem -> Experiment Mapping`
- `How to Write Technical Notes`
- `How to Prepare a Reproducible Math/ML Study`

### 9. Dashboard

Optional for later.

Useful features:

- progress
- completed modules
- paper queue
- saved notes
- spaced review cards

## Module Template

Every teaching module should follow the same page shape.

## Suggested Content Tree

If you build this in a static site or content-driven app, a clean structure is:

```text
content/
  home/
    index.md
  start-here/
    index.md
    placement-check.md
    notation-guide.md
    how-to-study-proofs.md
    how-to-read-theory-papers.md
  roadmaps/
    core-math-foundation.md
    ai-ml-theory.md
    engineering-systems.md
    paper-reading.md
  foundations/
    proofs-mathematical-thinking/
      index.md
      concepts/
      proofs/
      exercises/
      paper-lab/
    discrete-math-logic/
      index.md
      concepts/
      proofs/
      exercises/
      paper-lab/
    single-variable-calculus/
      index.md
      concepts/
      exercises/
    linear-algebra/
      index.md
      concepts/
      proofs/
      exercises/
      paper-lab/
    multivariable-calculus/
      index.md
      concepts/
      exercises/
    probability/
      index.md
      concepts/
      proofs/
      exercises/
      paper-lab/
    statistics/
      index.md
      concepts/
      exercises/
      paper-lab/
    optimization/
      index.md
      concepts/
      proofs/
      exercises/
      paper-lab/
    numerical-linear-algebra/
      index.md
      concepts/
      exercises/
      paper-lab/
    real-analysis/
      index.md
      concepts/
      proofs/
      exercises/
      paper-lab/
    matrix-analysis/
      index.md
      concepts/
      proofs/
      exercises/
      paper-lab/
    high-dimensional-probability-statistics/
      index.md
      concepts/
      proofs/
      exercises/
      paper-lab/
  paper-lab/
    index.md
    three-pass-reading.md
    theorem-decoder.md
    notation-translation.md
    assumption-checklist.md
    dependency-map.md
  practice/
    index.md
    proof-drills.md
    computation-drills.md
    mini-capstones.md
  library/
    index.md
    books/
    papers/
  research-workflow/
    index.md
    theory-writing.md
    reading-tracker.md
    claim-theorem-experiment.md
  specializations/
    federated-learning-low-rank/
      index.md
```

## Suggested URL Pattern

Recommended URL rules:

- track pages: `/roadmaps/<track-slug>`
- module pages: `/foundations/<module-slug>`
- concept pages: `/foundations/<module-slug>/concepts/<concept-slug>`
- proof pages: `/foundations/<module-slug>/proofs/<proof-slug>`
- exercise pages: `/foundations/<module-slug>/exercises/<exercise-slug>`
- paper pages: `/foundations/<module-slug>/paper-lab/<paper-slug>`
- source pages: `/library/books/<book-slug>` and `/library/papers/<paper-slug>`

This keeps the site teachable, searchable, and expandable without reorganizing later.

### Track Page

Include:

- audience
- prerequisites
- target outcomes
- recommended pacing
- exit criteria

### Module Page

Include:

- why this topic matters for `CS / AI / engineering`
- prerequisites
- core ideas
- theorem list
- proof patterns
- exercise ladder
- paper-reading bridge
- source books

### Concept Page

Include:

- intuition
- formal definitions
- key theorems
- worked examples
- failure modes and common mistakes
- where it appears in papers

### Proof Page

Include:

- statement
- proof strategy
- annotated proof
- stripped-down proof skeleton
- alternate proof if useful
- checklist for writing similar proofs

### Exercise Page

Include:

- warm-up problems
- core problems
- proof problems
- computation problems
- challenge problems
- hints and full solutions

### Paper Lab Page

Include:

- first pass
- second pass
- third pass
- notation map
- theorem dependency graph
- hidden prerequisites
- one reproduction task

## Suggested Learning Roadmap

This roadmap is for someone aiming at deep research fluency, not just coursework survival.

### Phase 0: Study Skills and Repair

Goal:

- stop getting blocked by notation and proof style

Focus:

- logic
- sets
- functions
- proof structure
- algebra refresh
- calculus refresh

Exit criteria:

- can write induction, contradiction, contrapositive, and direct proofs
- can read a theorem and identify assumptions, conclusion, and quantifiers

### Phase 1: Core Computational Foundations

Goal:

- become fluent with the math used everywhere in ML and engineering

Focus:

- linear algebra
- single-variable calculus
- multivariable calculus
- vectors, matrices, derivatives, gradients, Jacobians, Hessians

Exit criteria:

- can derive common gradients
- can reason about eigenvalues, SVD, projections, and least squares
- can read basic optimization derivations

### Phase 2: Uncertainty and Algorithms

Goal:

- move from deterministic calculus into statistical reasoning

Focus:

- probability
- statistics
- optimization
- numerical methods

Exit criteria:

- can follow concentration-style arguments at a basic level
- can read ERM, regularization, generalization, and convex optimization papers with support
- can distinguish exact math from numerical approximation issues

### Phase 3: Mathematical Maturity Upgrade

Goal:

- become comfortable with the style of rigorous theory papers

Focus:

- real analysis
- rigorous linear algebra / matrix analysis
- proof-heavy derivations

Exit criteria:

- can read and rewrite proofs with precision
- can understand continuity, compactness, convergence, norms, operator bounds
- can see why assumptions are needed

### Phase 4: Research-Level Theory

Goal:

- specialize into the math that shows up in advanced ML and engineering theory

Focus:

- matrix analysis
- convex optimization
- high-dimensional probability
- high-dimensional statistics
- learning theory
- stochastic processes if needed
- information theory or control if needed

Exit criteria:

- can read a heavy theory paper in multiple passes without losing the thread
- can extract lemma dependencies
- can map a theorem to its experiment or algorithmic implication

## How to Use Your Local Library

### Beginner Seed

Use:

- `/Users/mitu/Desktop/data/math/books/math-for-beginner/math.tex`
- `The Matrix Cookbook.pdf` as an appendix, not a main teacher

Important note:

This is not yet enough for a full beginner track by itself.

### Intermediate Shelf

Use:

- `Introductory Lectures on Convex Optimization.pdf`
- `Understanding Machine Learning From Theory to Algorithms.pdf`
- `Numerical linear algebra.pdf`
- selected chapters from `Foundations_of_Machine_Learning.pdf`

Best role:

- bridge from course-style foundations into research-facing math

### Advanced Shelf

Use:

- `Convex Optimization.pdf`
- `Matrix Analysis.pdf`
- `High-Dimensional Probability.pdf`
- `High-Dimensional Statistics-short.pdf`
- `High-Dimensional Statistics.pdf`
- selected theory chapters from `The Elements of Statistical Learning.pdf`

Best role:

- advanced modules
- paper support
- reference pages

### Specialization Shelf

Use:

- `dm.pdf` for decision-making / RL
- `fl-lora-acm/*`
- `fl-lora-related-work/*`

Best role:

- `Paper Lab`
- specialization track
- research workflow examples

Do not present authoring artifacts as learning sources:

- `acmart-package/*`
- sample conference PDFs
- figure exports
- archived drafts

## Best Way to Reuse `math.tex`

Your local handbook is already close to a web curriculum.

Strong reusable parts:

- objective-first structure
- prerequisites and self-checks
- worked examples
- pillar-based organization
- theory reading workflow

Recommended transformation:

- keep `Module I` as the main backbone
- move FL/privacy/robustness into specialization
- split `Module II` into `Practice Labs`
- split `Module III` into `Research Workflow`
- turn the "12 extra knowledge blocks" into future expansion topics

## First 20 Pages To Publish

Start with pages that create a usable learning spine fast.

1. Home
2. Start Here
3. Placement Check
4. How to Study Proofs
5. How to Read Theory Papers
6. Core Math Foundation Roadmap
7. Proofs and Mathematical Thinking
8. Discrete Math and Logic
9. Single-Variable Calculus
10. Linear Algebra
11. Multivariable Calculus
12. Probability
13. Statistics
14. Optimization
15. Numerical Linear Algebra
16. Real Analysis
17. Matrix Analysis
18. Paper Lab
19. Library
20. Research Workflow

## Recommended 12-Week Content Build Plan

### Weeks 1-2

Build:

- Home
- Start Here
- Placement Check
- Notation Guide
- Core Roadmap

### Weeks 3-4

Build:

- Proofs and Mathematical Thinking
- Discrete Math and Logic
- How to Read Theory Papers

### Weeks 5-6

Build:

- Linear Algebra
- Single-Variable Calculus
- Multivariable Calculus

### Weeks 7-8

Build:

- Probability
- Statistics
- Optimization

### Weeks 9-10

Build:

- Numerical Linear Algebra
- Real Analysis
- Paper Lab starter pages

### Weeks 11-12

Build:

- Matrix Analysis
- ML Theory bridge pages
- Library metadata pages for your local books

## Recommended Source Backbone

Use official or author-maintained resources as the main external scaffold.

- MIT `Mathematics for Computer Science`
- MIT `18.06 Linear Algebra`
- MIT `18.01 Single Variable Calculus`
- MIT `18.02 Multivariable Calculus`
- MIT `Introduction to Probability`
- MIT `18.100A Introduction to Analysis`
- MIT `18.065 Matrix Methods in Data Analysis, Signal Processing, and Machine Learning`
- MIT `18.657 Mathematics of Machine Learning`
- Stanford `EE364a Convex Optimization I`
- Stanford `CS103 Guide to Proofs`
- Stanford `EE364m The Mathematics of Convexity`
- Stanford `CS167 Paper-Reading Survival Kit`
- `Mathematics for Machine Learning`

## Why This Structure Works

It matches how strong technical curricula are usually organized:

- proofs and discrete thinking are introduced early
- linear algebra and calculus are parallel, not strictly serial
- probability comes before advanced statistics
- optimization and numerical methods are treated as central, not optional
- real analysis acts as the maturity upgrade for reading theory-heavy work
- paper reading is treated as a skill with its own workflow, not something that happens automatically after coursework

## Final Recommendation

If you want this site to become genuinely valuable, treat it as:

- a curriculum
- a reference
- a paper-reading assistant
- a research workflow system

not just a bookshelf website.

That is the difference between a nice archive and a real long-term learning engine.

## Sources

- MIT Mathematics for Computer Science: https://ocw.mit.edu/courses/6-1200j-mathematics-for-computer-science-spring-2024/
- MIT Linear Algebra: https://ocw.mit.edu/courses/18-06sc-linear-algebra-fall-2011/
- MIT Single Variable Calculus: https://ocw.mit.edu/courses/18-01sc-single-variable-calculus-fall-2010/
- MIT Multivariable Calculus: https://ocw.mit.edu/courses/18-02sc-multivariable-calculus-fall-2010/
- MIT Introduction to Probability: https://ocw.mit.edu/courses/res-6-012-introduction-to-probability-spring-2018/
- MIT Introduction to Analysis: https://ocw.mit.edu/courses/18-100a-introduction-to-analysis-fall-2012/
- MIT Matrix Methods in Data Analysis, Signal Processing, and Machine Learning: https://ocw.mit.edu/courses/18-065-matrix-methods-in-data-analysis-signal-processing-and-machine-learning-spring-2018/
- MIT Mathematics of Machine Learning: https://www.ocw.mit.edu/courses/18-657-mathematics-of-machine-learning-fall-2015/
- Stanford EE364a Convex Optimization I: https://web.stanford.edu/class/ee364a/index.html
- Stanford EE364m The Mathematics of Convexity: https://web.stanford.edu/class/ee364m/
- Stanford CS103 Guide to Proofs: https://web.stanford.edu/class/archive/cs/cs103/cs103.1254/guide_to_proofs
- Stanford CS167 Paper-Reading Survival Kit: https://cs.stanford.edu/~rishig/courses/ref/paper-reading-technical.pdf
- Stanford WIM Guidance: https://mathematics.stanford.edu/wim-guidance
- Mathematics for Machine Learning: https://mml-book.github.io/
- CMU 10-702 Statistical Machine Learning: https://www.cs.cmu.edu/~10702/
