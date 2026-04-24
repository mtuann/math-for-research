# Math Foundation Reference Roadmap

## Purpose

This roadmap is for building a `deep, research-ready math foundation` for:

- `CS`
- `AI / ML`
- `engineering`
- `theory-heavy paper reading`

It is not organized as a fixed `12-month plan`.

Instead, it is organized as a `dependency-aware learning ladder` with strong references for each topic.

For each topic, use this pattern:

- `First pass`: build intuition, notation, and basic fluency
- `Second pass`: deepen rigor, proofs, exercises, and abstraction
- `Research bridge`: connect to papers, advanced notes, or specialized theory

## How To Use This Roadmap

For every topic, try to have:

1. one `official course spine`
2. one `book or notes` source
3. one `practice / repair` source
4. one `advanced / second-pass` source

Do not try to consume every resource fully.

A better pattern is:

- pick `1 primary resource`
- keep `1 secondary perspective`
- use `1 repair source` when stuck

If you want the roadmap to feel closer to `UIUC`, use the `UIUC backbone` below as your campus-aligned sequence, then supplement it with the public notes/books in each topic section.

## Global Order

1. `Algebra repair`
2. `Proof writing`
3. `Logic`
4. `Discrete math`
5. `Single-variable calculus`
6. `Linear algebra`
7. `Multivariable calculus`
8. `ODE and dynamical systems basics`
9. `Probability`
10. `Statistics and inference`
11. `Real analysis`
12. `Optimization`
13. `Numerical methods`
14. `Matrix analysis`
15. `Learning theory`
16. `High-dimensional probability`
17. `High-dimensional statistics`
18. `Optional branch: information theory`
19. `Optional branch: control`

Overlay this through the whole journey:

- `paper-reading method`

## UIUC Backbone

If you want a `UIUC-flavored path`, this is the cleanest campus-aligned sequence:

1. [MATH 347 Fundamental Mathematics](https://math.illinois.edu/resources/syllabus-math-347)
2. [CS 173 Discrete Structures](https://courses.grainger.illinois.edu/cs173/)
3. [MATH 241 Calculus III](https://math.illinois.edu/resources/syllabus-math-241)
4. [MATH 257 Linear Algebra with Computational Applications](https://courses.illinois.edu/schedule/DEFAULT/DEFAULT/MATH/257)
5. [MATH 285 Differential Equations](https://math.illinois.edu/resources/syllabus-math-285)
6. [CS/STAT 361 Probability and Statistics for Computer Science](https://courses.illinois.edu/schedule/2026/spring/CS/361)
7. [MATH 416 Abstract Linear Algebra](https://netmath.illinois.edu/college/math-416)
8. [MATH 444 Elementary Real Analysis](https://netmath.illinois.edu/college/math-444)
9. [MATH 447 Real Variables](https://netmath.illinois.edu/college/math-447)
10. [IE 310 Deterministic Models in Optimization](https://ws.engr.illinois.edu/courses/getfile.asp?id=806) or [IE 521 Convex Optimization](https://courses.grainger.illinois.edu/ie521/fa2024/)

This backbone is especially good if you want:

- a roadmap that matches `UIUC course culture`
- a smoother transition into `Illinois research groups`
- a practical map from `undergraduate core -> proof maturity -> theory readiness`

## 1. Algebra Repair

Study carefully:

- arithmetic with symbols
- equations and inequalities
- functions
- factoring
- exponentials and logarithms
- trigonometric basics
- sequences and elementary modeling

Best references:

- [OpenStax Elementary Algebra 2e](https://openstax.org/books/elementary-algebra-2e/pages/1-introduction) `First pass if fundamentals are shaky`
- [OpenStax Intermediate Algebra 2e](https://openstax.org/books/intermediate-algebra-2e/pages/1-introduction) `First pass`
- [Paul’s Online Notes: Algebra and Trig Review](https://tutorial.math.lamar.edu/Extras/AlgebraTrigReview/AlgebraTrig.aspx) `Repair source`
- [OpenStax College Algebra 2e](https://openstax.org/books/college-algebra-2e/pages/index) `Second pass`
- [OpenStax Precalculus 2e](https://openstax.org/books/precalculus-2e/pages/preface) `Second pass`

Best use:

- `OpenStax` for complete rebuild
- `Paul’s Notes` for quick patching and worked examples

UIUC note:

- UIUC does not have a single signature public course here that works as a better self-study replacement than the open algebra/precalculus sources above, so I would keep the external resources for this stage.

## 2. Proof Writing

Study carefully:

- direct proof
- contrapositive
- contradiction
- induction
- quantified statements
- writing clear theorem-proof structure

Best references:

- [Stanford CS103: Mathematical Proofs](https://web.stanford.edu/class/archive/cs/cs103/cs103.1266/lectures/01/) `First pass`
- [Stanford CS103 Proofwriting Checklist](https://web.stanford.edu/class/cs103/proofwriting_checklist) `Ongoing`
- [Book of Proof](https://richardhammack.github.io/BookOfProof/index.html) `First pass`
- [PLP: A First Course in Mathematical Proof](https://personal.math.ubc.ca/~PLP/) `First or second pass`
- [An Infinite Descent into Pure Mathematics](https://infinitedescent.xyz/) `Second pass`

Best use:

- `Stanford CS103` for practical proof habits
- `Book of Proof` for structured self-study
- `PLP` for a full course-style treatment with supporting materials

UIUC equivalent:

- [MATH 347 Fundamental Mathematics](https://math.illinois.edu/resources/syllabus-math-347) `Best UIUC proof/maturity anchor`

## 3. Logic

Study carefully:

- propositional logic
- predicates and quantifiers
- negation
- implication and equivalence
- proof rules
- translating English into formal statements

Best references:

- [CMU OLI Logic and Proofs](https://oli.cmu.edu/courses/logic-proofs/) `First pass`
- [CMU Discrete Math Primer](https://www.csd.cmu.edu/course/15051/m25) `Gentle bridge`
- [Stanford CS103 Guide to Translation](https://web.stanford.edu/class/cs103/guide_to_translation) `Ongoing`
- [Stanford CS103 Guide to Negation](https://web.stanford.edu/class/cs103/guide_to_negation) `Ongoing`
- [forall x: Calgary](https://forallx.openlogicproject.org/) `Second pass`
- [Sets, Logic, Computation](https://slc.openlogicproject.org/) `Second pass`

UIUC equivalent:

- [MATH 347 Fundamental Mathematics](https://math.illinois.edu/resources/syllabus-math-347) `Logic, quantifiers, proof language, sets, functions`

## 4. Discrete Math

Study carefully:

- sets and functions
- relations
- combinatorics
- recurrences
- graphs
- asymptotics
- elementary probability
- number theory basics

Best references:

- [MIT Mathematics for Computer Science, Spring 2024](https://ocw.mit.edu/courses/6-1200j-mathematics-for-computer-science-spring-2024/) `Best broad official spine`
- [CMU 15-151, Fall 2025](https://www.csd.cmu.edu/course/15151/f25) `Proof-heavy perspective`
- [Stanford CS103, Spring 2026](https://web.stanford.edu/class/cs103/) `Proof + CS theory bridge`
- [UC Berkeley CS70, Spring 2026](https://www.eecs70.org/) `Algorithmic and probability flavor`
- [Discrete Mathematics: An Open Introduction](https://discrete.openmathbooks.org/) `Friendly book companion`

UIUC equivalent:

- [CS 173 Discrete Structures](https://courses.grainger.illinois.edu/cs173/) `Best UIUC discrete math/CS theory bridge`

## 5. Single-Variable Calculus

Study carefully:

- limits
- continuity
- derivatives
- integrals
- series
- Taylor expansion
- optimization and modeling

Best references:

- [MIT 18.01 Calculus I](https://www.ocw.mit.edu/courses/18-01-calculus-i-single-variable-calculus-fall-2020/) `Best first-pass course spine`
- [Active Calculus](https://activecalculus.org/) `Best if you learn by doing`
- [OpenStax Calculus Volume 1](https://openstax.org/books/calculus-volume-1/pages/preface) `Reference + exercises`
- [MIT 18.01SC Single Variable Calculus](https://ocw.mit.edu/courses/18-01sc-single-variable-calculus-fall-2010/) `Second pass`
- [Paul’s Online Notes](https://tutorial.math.lamar.edu/) `Repair source`

UIUC note:

- UIUC’s most relevant campus-calculus anchor for later theory work is [MATH 241 Calculus III](https://math.illinois.edu/resources/syllabus-math-241), so for single-variable calculus I would still primarily use the external calculus resources above.

## 6. Linear Algebra

Study carefully:

- vectors
- subspaces
- bases
- linear maps
- matrix factorization
- least squares
- eigenvalues and eigenvectors
- orthogonality
- SVD

Best references:

- [MIT 18.06SC Linear Algebra](https://ocw.mit.edu/courses/18-06sc-linear-algebra-fall-2011/) `Best first-pass official course`
- [Hefferon’s Linear Algebra](https://hefferon.net/linearalgebra/) `Best self-study companion`
- [Stanford Math 51](https://web.stanford.edu/class/math51/) `Integrated CS/engineering perspective`
- [Linear Algebra Done Right](https://linear.axler.net/) `Second pass, proof-heavy`
- [Immersive Linear Algebra](https://immersivemath.com/ila/) `Visual and interactive perspective`

Best use:

- `MIT 18.06SC + Hefferon` for first pass
- `Axler` once you want operator-level understanding

UIUC equivalents:

- [MATH 257 Linear Algebra with Computational Applications](https://courses.illinois.edu/schedule/DEFAULT/DEFAULT/MATH/257) `Applied first pass`
- [MATH 416 Abstract Linear Algebra](https://netmath.illinois.edu/college/math-416) `Proof-heavy second pass`

## 7. Multivariable Calculus

Study carefully:

- partial derivatives
- gradients
- Jacobians
- Hessians
- multiple integrals
- vector fields
- constrained optimization

Best references:

- [MIT 18.02SC Multivariable Calculus](https://ocw.mit.edu/courses/18-02sc-multivariable-calculus-fall-2010/) `Best self-study spine`
- [Stanford Math 51](https://web.stanford.edu/class/math51/) `Big-picture linear algebra view`
- [Active Calculus Multivariable](https://activecalculus.org/acm/) `Activity-based perspective`
- [OpenStax Calculus Volume 3](https://openstax.org/books/calculus-volume-3/pages/preface) `Reference`
- [Paul’s Calculus III Notes](https://tutorial.math.lamar.edu/classes/calciii/calciii.aspx) `Repair source`

UIUC equivalent:

- [MATH 241 Calculus III](https://math.illinois.edu/resources/syllabus-math-241) `Best UIUC multivariable/vector calculus anchor`

## 8. ODE and Dynamical Systems Basics

Study carefully:

- first-order ODEs
- second-order ODEs
- linear systems
- matrix exponential
- phase portraits
- stability
- nonlinear dynamics intuition

Best references:

- [MIT 18.03 Differential Equations](https://www.ocw.mit.edu/courses/18-03-differential-equations-spring-2010/resources/lecture-notes/) `Best engineering-style first pass`
- [Notes on Diffy Qs](https://www.jirka.org/diffyqs/) `Excellent free text`
- [AIM Ordinary Differential Equations Project](https://textbooks.aimath.org/textbooks/approved-textbooks/judson-odes/) `Computation and activities`
- [Steven Strogatz Teaching Page](https://www.stevenstrogatz.com/teaching) `Second pass intuition`
- [Herman: A Second Course in ODEs](https://math.libretexts.org/Bookshelves/Differential_Equations/A_Second_Course_in_Ordinary_Differential_Equations%3A_Dynamical_Systems_and_Boundary_Value_Problems_%28Herman%29) `Bridge to systems`

UIUC equivalent:

- [MATH 285 Differential Equations](https://math.illinois.edu/resources/syllabus-math-285) `Best UIUC ODE anchor`

## 9. Probability

Study carefully:

- random variables
- conditional probability
- Bayes rule
- expectation
- variance and covariance
- distributions
- LLN and CLT
- concentration basics
- Markov chains

Best references:

- [Harvard Stat 110](https://stat110.hsites.harvard.edu/) `Best first-pass intuition`
- [MIT RES.6-012 Introduction to Probability](https://ocw.mit.edu/courses/res-6-012-introduction-to-probability-spring-2018/) `Compact engineering treatment`
- [Stanford Stats 116](https://web.stanford.edu/class/stats116/) `Clean modern notes`
- [MIT 6.041 Probabilistic Systems Analysis](https://ocw.mit.edu/courses/6-041-probabilistic-systems-analysis-and-applied-probability-fall-2010/) `Second pass`
- [Berkeley EECS 126](https://www2.eecs.berkeley.edu/Courses/EECS126/) `Best CS/EE bridge`

UIUC equivalent:

- [CS/STAT 361 Probability and Statistics for Computer Science](https://courses.illinois.edu/schedule/2026/spring/CS/361) `Best UIUC probability/statistics bridge for CS`

## 10. Statistics and Inference

Study carefully:

- estimation
- likelihood
- bias and variance
- confidence intervals
- hypothesis testing
- Bayesian vs frequentist viewpoints
- linear models
- bootstrap and nonparametric intuition

Best references:

- [MIT 18.05 Introduction to Probability and Statistics](https://ocw.mit.edu/courses/18-05-introduction-to-probability-and-statistics-spring-2022/) `Strong undergraduate bridge`
- [Stanford Stats 200](https://edit-summer.stanford.edu/sites/summer/files/media/file/stats200_syllabus_summer-2025.pdf) `Mathematically grounded inference`
- [CMU 36-700 Probability and Mathematical Statistics I](https://www.stat.cmu.edu/~siva/teaching/700/) `Best bridge to theory`
- [CMU 36-705 Intermediate Statistics](https://stat.cmu.edu/~siva/teaching/705/) `Second pass`
- [All of Statistics](https://www.stat.cmu.edu/~larry/all-of-statistics/index.html) `Compact reference`
- [OpenIntro Statistics](https://www.openintro.org/book/os/) `Gentler practical companion`

UIUC equivalent:

- [CS/STAT 361 Probability and Statistics for Computer Science](https://courses.illinois.edu/schedule/2026/spring/CS/361) `Main UIUC inference bridge`

## 11. Real Analysis

Study carefully:

- rigorous limits
- convergence
- continuity
- compactness
- completeness
- sequences and series
- function sequences
- proof structure around epsilon arguments

Best references:

- [MIT 18.100A Real Analysis](https://ocw.mit.edu/courses/18-100a-real-analysis-fall-2020/) `Official course spine`
- [Basic Analysis — Jiří Lebl](https://www.jirka.org/ra/) `Best free self-study text`
- [Understanding Analysis — Stephen Abbott](https://link.springer.com/book/10.1007/978-0-387-21506-8) `Best intuition-to-rigor bridge`
- [Analysis I — Terence Tao](https://terrytao.wordpress.com/books/analysis-i/) `Second pass`
- [Analysis II — Terence Tao](https://terrytao.wordpress.com/books/analysis-ii/) `Second pass`

Best use:

- `Abbott or Lebl + MIT 18.100A` for first pass
- `Tao` for deeper second pass

UIUC equivalents:

- [MATH 444 Elementary Real Analysis](https://netmath.illinois.edu/college/math-444) `Best first UIUC analysis course`
- [MATH 447 Real Variables](https://netmath.illinois.edu/college/math-447) `Stronger UIUC theory track`

## 12. Optimization

Study carefully:

- convex sets and functions
- duality
- KKT conditions
- gradient methods
- stochastic methods
- proximal methods
- convergence
- complexity intuition

Best references:

- [Stanford EE364A Convex Optimization I](https://web.stanford.edu/class/ee364a/) `Best first-pass course`
- [Convex Optimization — Boyd and Vandenberghe](https://stanford.edu/~boyd/cvxbook/) `Canonical text`
- [MIT 6.253 Convex Analysis and Optimization](https://web.mit.edu/6.253/www/) `Second pass, proof-oriented`
- [Introductory Lectures on Convex Optimization — Nesterov](https://link.springer.com/book/10.1007/978-1-4419-8853-9) `Second pass`
- [Convex Optimization: Algorithms and Complexity — Bubeck](https://arxiv.org/abs/1405.4980) `CS-style theory`
- [Introduction to Online Convex Optimization — Hazan](https://mitpress.mit.edu/9780262046985/introduction-to-online-convex-optimization/) `ML theory branch`

Local books:

- [Convex Optimization.pdf](</Users/mitu/Desktop/data/math/books/Convex Optimization.pdf>) `Excellent second-pass anchor`
- [Introductory Lectures on Convex Optimization.pdf](</Users/mitu/Desktop/data/math/books/Introductory Lectures on Convex Optimization.pdf>) `Useful bridge`

UIUC equivalents:

- [IE 310 Deterministic Models in Optimization](https://ws.engr.illinois.edu/courses/getfile.asp?id=806) `Best undergraduate optimization bridge`
- [IE 521 Convex Optimization](https://courses.grainger.illinois.edu/ie521/fa2024/) `Best rigorous UIUC convex optimization route`

## 13. Numerical Methods

Study carefully:

- conditioning
- stability
- floating-point issues
- interpolation
- numerical integration
- iterative methods
- error analysis
- scientific computing viewpoint

Best references:

- [MIT 18.335 Numerical Methods of Applied Mathematics](https://web.mit.edu/course/18/18.335/WWW/) `Graduate course spine`
- [Fundamentals of Numerical Computation](https://tobydriscoll.net/book/fnc/) `Best open self-study text`
- [Numerical Linear Algebra — Trefethen and Bau](https://people.maths.ox.ac.uk/trefethen/text.html) `Bridge into numerical LA`
- [Accuracy and Stability of Numerical Algorithms — Higham](https://nhigham.com/accuracy-and-stability-of-numerical-algorithms/) `Second pass`
- [UC Berkeley Math 221](https://people.eecs.berkeley.edu/~demmel/ma221_Fall04/) `Rigorous numerical linear algebra`
- [UC Berkeley CS267](https://people.eecs.berkeley.edu/~demmel/cs267/) `Large-scale computing branch`

Local books:

- [Numerical linear algebra.pdf](</Users/mitu/Desktop/data/math/books/Numerical linear algebra.pdf>) `Strong second-pass anchor`

## 14. Matrix Analysis

Study carefully:

- matrix norms
- PSD matrices
- operator inequalities
- perturbation bounds
- spectral tools
- singular values
- low-rank structure

Best references:

- [Joel Tropp, Matrix Analysis notes](https://tropp.caltech.edu/notes/Tro22-Matrix-Analysis-LN.pdf) `Best modern bridge`
- [MIT 18.065 Matrix Methods](https://ocw.mit.edu/courses/18-065-matrix-methods-in-data-analysis-signal-processing-and-machine-learning-spring-2018/) `Applied bridge`
- [Rajendra Bhatia, Matrix Analysis](https://link.springer.com/book/10.1007/978-1-4612-0653-8) `Elegant second pass`
- [Horn and Johnson, Matrix Analysis](https://www.cambridge.org/highereducation/books/matrix-analysis/FDA3627DC2B9F5C3DF2FD8C3CC136B48) `Canonical reference`
- [Positive Definite Matrices — Bhatia](https://www.degruyterbrill.com/document/doi/10.1515/9781400827787/html) `PSD specialization`

Local books:

- [Matrix Analysis.pdf](</Users/mitu/Desktop/data/math/books/Matrix Analysis.pdf>) `Strong second-pass anchor`
- [The Matrix Cookbook.pdf](</Users/mitu/Desktop/data/math/books/The Matrix Cookbook.pdf>) `Formula/reference only`

## 15. Learning Theory

Study carefully:

- ERM
- VC and PAC ideas
- generalization
- regularization
- stability
- surrogate losses
- modern generalization debates

Best references:

- [MIT 18.657 Mathematics of Machine Learning](https://www.ocw.mit.edu/courses/18-657-mathematics-of-machine-learning-fall-2015/) `Rigorous course bridge`
- [Stanford CS229](https://cs229.stanford.edu/) `Applied ML theory bridge`
- [Stanford CS229T Statistical Learning Theory](https://web.stanford.edu/class/cs229t/) `Second pass`
- [Understanding Machine Learning](https://www.cambridge.org/core/books/understanding-machine-learning/3059695661405D25673058E43C8BE2A6) `Best broad entry`
- [Foundations of Machine Learning](https://mitpress.mit.edu/9780262039406/foundations-of-machine-learning/) `Best long-term reference`
- [Learnability, Stability and Uniform Convergence](https://www.jmlr.org/papers/v11/shalev-shwartz10a.html) `Key paper`
- [Understanding Deep Learning Requires Rethinking Generalization](https://arxiv.org/abs/1611.03530) `Modern tension point`

UIUC equivalent:

- [CS 446/ECE 449 Machine Learning](https://courses.grainger.illinois.edu/cs446/) `Applied ML bridge with theory components`

Local books:

- [Understanding Machine Learning From Theory to Algorithms.pdf](</Users/mitu/Desktop/data/math/books/Understanding Machine Learning From Theory to Algorithms.pdf>)
- [Foundations_of_Machine_Learning.pdf](</Users/mitu/Desktop/data/math/books/Foundations_of_Machine_Learning.pdf>)
- [The Elements of Statistical Learning.pdf](</Users/mitu/Desktop/data/math/books/The Elements of Statistical Learning.pdf>)

## 16. High-Dimensional Probability

Study carefully:

- sub-Gaussian and sub-exponential behavior
- concentration inequalities
- random matrices
- covering arguments
- geometric viewpoint

Best references:

- [Roman Vershynin’s High-Dimensional Probability course](https://www.math.uci.edu/~rvershyn/teaching/hdp/hdp.html) `Best first-pass course`
- [High-Dimensional Probability book page](https://www.math.uci.edu/~rvershyn/papers/HDP-book/HDP-book.html) `Author page`
- [Princeton Probability in High Dimension](https://orfe.princeton.edu/courses/spring-2024/topics-probability-probability-high-dimension) `Complementary advanced course`
- [Ramon van Handel notes](https://web.math.princeton.edu/~rvan/APC550.pdf) `Deep second pass`
- [Four Lectures on Probabilistic Methods for Data Science](https://arxiv.org/abs/1612.06661) `Bridge note`
- [Estimation in High Dimensions: A Geometric Perspective](https://arxiv.org/abs/1405.5103) `Bridge note`

Local books:

- [High-Dimensional Probability.pdf](</Users/mitu/Desktop/data/math/books/High-Dimensional Probability.pdf>)

## 17. High-Dimensional Statistics

Study carefully:

- sparsity
- high-dimensional regression
- non-asymptotic bounds
- inference after regularization
- minimax ideas
- compressed sensing style arguments

Best references:

- [MIT 18.S997 High-Dimensional Statistics notes](https://ocw.mit.edu/courses/18-s997-high-dimensional-statistics-spring-2015/619e4ae252f1b26cbe0f7a29d5932978_MIT18_S997S15_CourseNotes.pdf) `First pass`
- [Simons Institute High-Dimensional Statistics](https://simons.berkeley.edu/high-dimensional-statistics) `Lecture set`
- [Wainwright, High-Dimensional Statistics](https://www.cambridge.org/core/books/highdimensional-statistics/8A91ECEEC38F46DAB53E9FF8757C7A4E) `Best second-pass book`
- [High-Dimensional Inference: Confidence Intervals, p-Values and R Software hdi](https://arxiv.org/abs/1408.4026) `Research bridge`
- [Stanford High-Dimensional Statistics research page](https://statistics.stanford.edu/research/high-dimensional-statistics) `Current perspective`

Local books:

- [High-Dimensional Statistics-short.pdf](</Users/mitu/Desktop/data/math/books/High-Dimensional Statistics-short.pdf>)
- [High-Dimensional Statistics.pdf](</Users/mitu/Desktop/data/math/books/High-Dimensional Statistics.pdf>)

## 18. Optional Branch: Information Theory

Take this if you care about:

- representation learning
- compression
- communication
- lower bounds
- inference and coding links

Best references:

- [Stanford EE276 Information Theory](https://web.stanford.edu/class/ee276) `Current official course`
- [Stanford EE376A](https://web.stanford.edu/class/ee376a/) `Classical first pass`
- [MIT 6.441 Information Theory notes](https://www.ocw.mit.edu/courses/6-441-information-theory-spring-2016/resources/lecture-notes/) `Second pass`
- [Information Theory: A Tutorial Introduction](https://arxiv.org/abs/1802.05968) `Friendly note`
- [Divergence, Entropy, Information](https://arxiv.org/abs/1708.07459) `Friendly note`
- [Shannon’s A Mathematical Theory of Communication](https://reach.ieee.org/wp-content/uploads/2023/05/IEEE_REACH_A_Mathematical_Theory_of_Communication.pdf) `Classic paper`

## 19. Optional Branch: Control

Take this if you care about:

- robotics
- systems
- RL
- sequential decision making
- stability and dynamics

Best references:

- [Stanford EE263 Introduction to Linear Dynamical Systems](https://see.stanford.edu/Course/EE263) `Best first systems language`
- [MIT Underactuated Robotics](https://underactuated.mit.edu/) `Best modern computational control bridge`
- [Stanford EE266 Stochastic Control](https://lall.stanford.edu/ee266/) `Second pass`
- [CMU 16-745 Optimal Control and Reinforcement Learning](https://optimalcontrol.ri.cmu.edu/) `Modern bridge to RL`

## Paper-Reading Overlay

Use this from the start, but especially from `optimization` onward.

Best references:

- [Keshav, How to Read a Paper](https://web.stanford.edu/class/cs245/readings/how-to-read-a-paper.pdf) `Core three-pass method`
- [Philip Levis, Reading a (CS or EE) Research Paper](https://web.stanford.edu/class/cs114/reading-levis.pdf) `Depth control`
- [Maria Stent, How to Read a Computer Science Research Paper](https://web.stanford.edu/class/cs114/reading-stent.pdf) `Structured reading`
- [Tim Roughgarden overview](https://cs.stanford.edu/~rishig/courses/ref/paper-reading-overview.pdf) `Theorem-heavy reading`
- [PLOS Ten Simple Rules for Reading a Scientific Paper](https://journals.plos.org/ploscompbiol/article?id=10.1371%2Fjournal.pcbi.1008032) `Cross-field advice`
- [Stanford CS114/214](https://stanford.edu/class/cs114/) `Reading seminar`

## Best Minimal Path

If you want one clean high-value path:

`algebra repair -> proof writing -> logic -> discrete math -> calculus -> linear algebra -> multivariable calculus -> probability -> statistics -> real analysis -> optimization -> numerical methods -> matrix analysis -> learning theory -> high-dimensional probability -> high-dimensional statistics`

## Best PhD-Theory Path

If your main goal is `reading heavy AI/ML/CS theory papers`:

`proof writing -> linear algebra -> multivariable calculus -> probability -> statistics -> real analysis -> optimization -> matrix analysis -> learning theory -> high-dimensional probability -> high-dimensional statistics`

## Best Use Of Your Local Shelf

Use your local books mostly as:

- `bridge texts` after basic courses
- `second-pass texts` after first exposure
- `reference books` during paper reading

Especially strong local matches:

- [Convex Optimization.pdf](</Users/mitu/Desktop/data/math/books/Convex Optimization.pdf>)
- [Foundations_of_Machine_Learning.pdf](</Users/mitu/Desktop/data/math/books/Foundations_of_Machine_Learning.pdf>)
- [Understanding Machine Learning From Theory to Algorithms.pdf](</Users/mitu/Desktop/data/math/books/Understanding Machine Learning From Theory to Algorithms.pdf>)
- [Matrix Analysis.pdf](</Users/mitu/Desktop/data/math/books/Matrix Analysis.pdf>)
- [Numerical linear algebra.pdf](</Users/mitu/Desktop/data/math/books/Numerical linear algebra.pdf>)
- [High-Dimensional Probability.pdf](</Users/mitu/Desktop/data/math/books/High-Dimensional Probability.pdf>)
- [High-Dimensional Statistics.pdf](</Users/mitu/Desktop/data/math/books/High-Dimensional Statistics.pdf>)

## Notes

- Current/actively maintained course pages and author pages were checked on `April 24, 2026`.
- Some excellent texts above are not free, but I included them when they are canonical and important.
- When a topic feels hard, prefer `one primary source + one repair source`, not five simultaneous sources.
- UIUC is now included as a `campus-aligned backbone`, but I still keep several MIT/Stanford/CMU/Berkeley resources because they are unusually strong for open self-study and public lecture-note access.
