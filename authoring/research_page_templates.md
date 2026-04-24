# Research-Facing Page Templates

Use this document as the strict house style for pages that connect math to applications, papers, and publication workflow.

These templates are for:
- `application` pages
- `paper-lab` pages
- `research-direction` pages
- `publication-workflow` pages

They are designed to keep the site:
- mathematically grounded
- useful for research reading
- current without becoming news-driven
- selective instead of turning into a link dump

## Shared Rules

### 1. Use live source verification before drafting

Before writing any research-facing page, do a fresh online check and record:

- `source-check-date`
- `last-reviewed`

Use absolute dates.

Minimum source pack:
- `1 stable source`: textbook, lecture notes, or classic paper for the math backbone
- `1 bridge source`: survey, tutorial, or course notes that connect the math to the area
- `2 recent primary sources`: representative papers from roughly the last `2-4` years when the area is active
- `1 official source` when relevant: venue page, benchmark page, artifact policy, or author instructions

Priority order:
1. official venue or organization pages
2. author-maintained papers, notes, and course pages
3. journal or proceedings pages
4. high-quality technical blogs only when they add real synthesis

Do not cite a blog when a stronger primary source exists.

### 2. Separate stable math from moving frontier

Every page must clearly distinguish:
- `Stable backbone`: definitions, lemmas, classical models, standard reductions
- `Active frontier`: current variants, open problems, recent shifts, unresolved tradeoffs

Do not present frontier claims as settled fact.

### 3. Keep a strict link budget

Default external link budget per page:
- `3-6 essential links`
- `0-3 optional links`

Every link must have a reason attached in prose:
- what it is
- why it is here
- what to look for

If a link has no annotation, remove it.

### 4. Write from math outward

Each page must answer all four questions:
1. `What is the mathematical object or tool?`
2. `Where does it appear in practice or research?`
3. `What assumptions make the connection valid?`
4. `What breaks when those assumptions fail?`

### 5. Prefer synthesis over coverage

Good page:
- explains a small number of ideas clearly
- shows one strong path through the literature
- gives readers a way to act: read, test, build, compare

Bad page:
- lists many papers with no map
- summarizes papers without math
- explains math with no research bridge

### 6. Use computation labs for code-heavy or interactive material

If a research-facing page needs substantial code, a simulation walkthrough, or a reactive visualization, pair it with a `computation-lab` page rather than forcing everything into the narrative page.

Use the narrative page to explain:

- the mathematical object
- the research question
- the assumptions
- the limits of the evidence

Use the paired `computation-lab` to show:

- code
- reproducible figures
- parameter sweeps
- simulation behavior
- numerical caveats

Every simulation or visual on a research-facing page must still say what mathematical claim, assumption, or failure mode it is illustrating.

### 7. Use the shared metadata contract

Use the field names from [contributing/page-templates.md](../contributing/page-templates.md). Do not invent a second schema.

```yaml
---
title: "..."
description: "..."
page-type: application | paper-lab | research-direction | publication-workflow
status: draft | published | archived
update-status: current | monitor | needs-refresh | major-refresh
level: foundation | advanced | research
topic: replace-me
prerequisites: []
learning-goals: []
applications: []
papers: []
keywords: []
maintainer: mtuann
last-reviewed: 2026-04-24
source-check-date: 2026-04-24
review-cadence: quarterly
date-modified: last-modified
draft: true
stable-sources: []
current-sources: []
---
```

`stable-sources` and `current-sources` are optional tracking fields for research-facing pages. They do not replace the required `Sources and Further Reading` section in the body.

## Template 1: Application Page

Purpose: show how a stable math idea becomes a real tool in CS, AI, or engineering.

### Required Sections

Sections must appear in this order.

1. `Application Snapshot`
   One short paragraph covering the problem, the math lever, and the main practical payoff.

2. `Problem Frame`
   State the task, objective, constraints, and success metric.

3. `Math Backbone`
   Name the exact objects, definitions, and theorems used. Keep this selective.

4. `Translation Layer`
   Explain how the math maps onto the application.
   Include approximations, relaxations, estimators, or modeling assumptions.

5. `Worked Mechanism`
   Walk through one concrete example, derivation, or algorithmic flow.

6. `Failure Modes`
   Explain where the method becomes fragile, misleading, or computationally expensive.

7. `Paper Bridge`
   Include:
   - `1 classic anchor`
   - `1 survey/tutorial/notes bridge`
   - `2 recent representative papers`
   For each item: say what math to watch for.

8. `Try It`
   Give one small experiment, derivation, or coding task.

9. `Source Guide`
   End with a short annotated reading path, not a bibliography dump.

### Optional Sections

- `Historical Note`
- `Implementation Note`
- `Dataset or Benchmark Note`
- `Theorem Map`
- `Linked Computation Lab`

### Forbidden Mistakes

- no application story without explicit math
- no code-heavy page with no assumptions discussion
- no “used everywhere” claims without examples
- no more than `4` papers in the main bridge
- no benchmarking language like `SOTA` unless the page is about evaluation and cites a current source

### Definition Of Done

The page is done when a reader can:
- describe the practical problem in one sentence
- identify the math object doing the work
- explain one key assumption
- name one failure mode
- follow one reading trail from math to papers

## Template 2: Paper Lab Page

Purpose: help a reader unpack one paper without losing the underlying math.

### Required Sections

Sections must appear in this order.

1. `Why This Paper`
   State why the paper is worth reading and what kind of reader it serves.

2. `Paper At A Glance`
   Give the paper type, setting, main claim, and one-sentence contribution summary.

3. `Reading Plan`
   Use the `first pass / second pass / third pass` structure.

4. `Prerequisite Math Map`
   List the minimum concepts needed, with links back into the site.

5. `Notation Table`
   Define only the symbols that actually block comprehension.

6. `Assumption Audit`
   List the assumptions that materially drive the result.

7. `Main Results Unpacked`
   For each central theorem, proposition, or result:
   - formal statement in plain language
   - intuition
   - proof or argument skeleton
   - why it matters

8. `Evidence Audit`
   Cover proof evidence, experiments, simulations, or ablations.
   State what supports the claim and what does not.

9. `What To Verify Yourself`
   Give one concrete reconstruction task:
   derivation, proof sketch, experiment, or figure reproduction.

10. `Context And Lineage`
   Place the paper among its predecessors and follow-ups.

11. `Transfer And Limits`
   Say where the result generalizes and where it likely does not.

12. `Resource Kit`
   Provide a short annotated list of prerequisites, companion notes, and follow-up reading.

### Optional Sections

- `Figure Guide`
- `Appendix Map`
- `Artifact Note`
- `Common Misreadings`
- `Linked Computation Lab`

### Forbidden Mistakes

- no paragraph-by-paragraph paraphrase
- no admiration-only summary without critique
- no unexplained theorem statements
- no skipping appendices when they contain core proofs or assumptions
- no more than `6` total external links unless the page is explicitly a survey trail

### Definition Of Done

The page is done when a reader can:
- state the main claim and setting from memory
- list the blocking prerequisites
- identify the key assumptions
- reconstruct at least one result at a high level
- explain what would need to be checked to trust the paper

## Template 3: Research Direction Page

Purpose: map an active area so readers can enter it through stable math rather than hype.

### Required Sections

Sections must appear in this order.

1. `Direction In One Paragraph`
   Define the area, the core question, and the mathematical center of gravity.

2. `Why It Matters`
   Explain the scientific or engineering pressure making the direction important.

3. `Stable Math Backbone`
   List the durable concepts and tools the area keeps reusing.

4. `Problem Families`
   Break the area into `3-5` recurring problem types.

5. `Current Frontier Map`
   Name the main subdirections that are currently active.

6. `Representative Reading Trail`
   Include:
   - `1 tutorial or survey`
   - `1 classic anchor`
   - `3-5 representative recent papers`
   Organize them as a path, not a flat list.

7. `How The Math Shows Up`
   Explain which theorems, proof patterns, or modeling ideas recur across papers.

8. `Evaluation Norms`
   State what counts as evidence in this direction:
   proof, theorem, benchmark, simulation, ablation, artifact, or system behavior.

9. `Open Problems`
   List a small number of concrete, non-generic research questions.

10. `Entry Projects`
   Suggest beginner, intermediate, and theory-heavy ways to enter the area.

11. `Watchpoints`
   Note misconceptions, overclaimed trends, or scope boundaries.

### Optional Sections

- `Timeline`
- `Glossary`
- `Venues And Labs`
- `Benchmark Table`

### Forbidden Mistakes

- no trend report with no math backbone
- no vague “hot area” language
- no stale paper list without a verification date
- no more than `7` papers in the main trail
- no “future work” bullets that could fit any field

### Definition Of Done

The page is done when a reader can:
- explain what defines the area
- name the math prerequisites
- separate stable ideas from active questions
- start reading with a short, justified paper trail
- articulate at least one real open problem

## Template 4: Publication Workflow Page

Purpose: teach one research-writing or submission skill in a way that connects claims, proofs, experiments, and reproducibility.

Examples:
- `claim-evidence matrix`
- `theorem-to-experiment alignment`
- `writing theory sections`
- `review and rebuttal`
- `artifact and reproducibility preparation`

### Required Sections

Sections must appear in this order.

1. `Workflow Goal`
   State the output of the workflow and when in the research cycle it matters.

2. `Inputs Required`
   List what must already exist: theorem statements, experimental results, draft figures, related work notes, code, appendix, or artifact.

3. `Decision Checkpoints`
   Give the `3-6` questions that decide whether the workflow is succeeding.

4. `Step-By-Step Process`
   Present a strict ordered workflow.

5. `Quality Bar`
   State what a skeptical reviewer should be able to verify after this workflow is done.

6. `Common Failure Modes`
   Include at least one theory-side failure and one experiment-side failure when relevant.

7. `Reproducibility And Artifact Expectations`
   Connect the workflow to proofs, appendices, code, data, compute details, and archival artifacts.

8. `Mini Template Or Checklist`
   End with something reusable:
   table, checklist, outline, or question set.

9. `Source Guide`
   Use a short annotated set of official venue or policy links.

### Optional Sections

- `Venue Variations`
- `Rebuttal Notes`
- `Collaboration Roles`
- `Timing Advice`
- `Ethics Or Broader-Impact Note`

### Forbidden Mistakes

- no prestige-chasing advice without technical substance
- no workflow that ignores reviewer verification
- no venue gossip
- no generic “write clearly” guidance without a process
- no submission advice that omits anonymity, appendix, or reproducibility concerns when relevant

### Definition Of Done

The page is done when a reader can:
- use the workflow on a real draft
- see what evidence each claim requires
- identify likely reviewer objections early
- know what must exist in paper, appendix, and artifact
- adapt the workflow across venues without rewriting the whole page

## Short Resource Policy

Use this annotation format for every external source:

- `Source`: what it is
- `Use it for`: what the reader should extract
- `Why this one`: why it beats nearby alternatives for this page

Default page mix:
- `1` stable math source
- `1` bridge source
- `2-5` current or representative papers
- `0-2` official workflow or venue sources

If you need more than this, split the page.

## Page Review Gate

Before publishing, verify all of the following:

- `The page names the math explicitly.`
- `The page has a current verification date.`
- `The page distinguishes stable material from active frontier.`
- `The page gives a reading path, not a dump of links.`
- `The page includes limits, assumptions, and failure modes.`
- `The page ends with a concrete next action for the reader.`

## Reference Backbone

These templates are aligned with a small set of durable references:
- [Quarto Interactivity Overview](https://quarto.org/docs/interactive/)
- [Quarto Observable JS](https://quarto.org/docs/interactive/ojs/)
- [Quarto Jupyter Widgets](https://quarto.org/docs/interactive/widgets/jupyter.html)
- [Keshav, *How to Read a Paper*](https://web.stanford.edu/class/cs114/reading-keshav.pdf)
- [Carey, Steiner, Petri, *Ten simple rules for reading a scientific paper*](https://journals.plos.org/ploscompbiol/article?id=10.1371%2Fjournal.pcbi.1008032)
- [Mensh and Kording, *Ten simple rules for structuring papers*](https://journals.plos.org/ploscompbiol/article?id=10.1371%2Fjournal.pcbi.1005619)
- [NeurIPS Paper Checklist](https://neurips.cc/public/guides/PaperChecklist)
- [ICML Paper Guidelines](https://icml.cc/Conferences/2023/PaperGuidelines)
- [ACM Artifact Review and Badging](https://www.acm.org/publications/policies/artifact-review-and-badging-current)
