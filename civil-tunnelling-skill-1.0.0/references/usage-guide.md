# Civil & Tunnelling Engineering — Usage Guide

This guide defines the end-to-end workflow for using the modular writing skill.

---

## 1. Decide the Task Before Editing

Identify both the section and the operation.

### Section

- Abstract
- Introduction
- Literature Review
- Site / Geology / Engineering Background
- Methods — experiment / field
- Methods — numerical / analytical
- Methods — TBM / operational data
- Results
- Discussion
- Conclusion
- Full paper

### Operation

- polish existing English;
- Chinese → English translation;
- restructure a paragraph;
- draft from supplied technical notes;
- audit style and technical clarity;
- check evidence strength and terminology.

Do not treat a request for language polishing as permission to change the science.

---

## 2. Lock Technical Content

Before editing, identify protected elements:

- numerical values;
- units;
- equations and LaTeX;
- variable names;
- figure/table/equation references;
- citations;
- tunnel/project names;
- geological units and classifications;
- material parameters;
- TBM/shield/EPB parameters;
- test conditions;
- initial/boundary conditions;
- dataset definitions;
- derived indicator definitions.

If the wording around a protected element is unclear, improve the prose around it rather than silently changing the element.

---

## 3. Identify Evidence Type

For each technical claim, determine whether it is based on:

- direct measurement;
- laboratory observation;
- field monitoring;
- numerical output;
- analytical derivation;
- derived quantity;
- statistical association;
- comparison with literature;
- interpretation/hypothesis;
- human-entered label.

The verb choice must match the evidence type.

---

## 4. Choose the Relevant Reference Files

### Introduction

Load:
- `sentence-templates.md` §§1–5;
- `paragraph-patterns.md` §§1–6.

### Site / Geology

Load:
- `sentence-templates.md` §6;
- `paragraph-patterns.md` §§3, 7–8;
- `phrase-bank.md` §§3–4 as needed.

### Experimental / Field Methods

Load:
- `sentence-templates.md` §§7–8;
- `paragraph-patterns.md` §§9–10;
- `meta-discourse.md` for data-quality boundaries.

### Numerical / Computational Methods

Load:
- `sentence-templates.md` §§9–10;
- `paragraph-patterns.md` §§11–14;
- `phrase-bank.md` §§2 and 8;
- `meta-discourse.md` §§5–6, 12–16.

### TBM / Shield / EPB

Load:
- `sentence-templates.md` §16;
- `phrase-bank.md` §4;
- `paragraph-patterns.md` §§25–27;
- `meta-discourse.md` §§2, 9, 11.

### Data-driven Engineering

Load:
- `sentence-templates.md` §17;
- `paragraph-patterns.md` §28;
- `meta-discourse.md` §§4, 9–11.

### Results / Discussion

Load:
- `sentence-templates.md` §§11–19;
- `paragraph-patterns.md` §§15–31;
- `meta-discourse.md` when interpretation requires boundaries.

### Translation

Load:
- `phrase-bank.md`;
- `sentence-templates.md` §21;
- this guide §§8–9.

---

## 5. Editing Workflow

### Pass 1 — Technical reading

Understand what the paragraph actually says. Resolve pronouns, variables and figure references before rewriting.

### Pass 2 — Structural diagnosis

Ask:

- What is this paragraph doing?
- Is the first sentence aligned with that function?
- Is evidence presented before interpretation?
- Are unrelated functions mixed together?
- Is the engineering object explicit?

### Pass 3 — Rewrite for engineering logic

Improve:

- subject clarity;
- information order;
- quantitative specificity;
- terminology consistency;
- relation between result and mechanism;
- relation between method and reproducibility.

### Pass 4 — Language polish

Improve:

- grammar;
- article/preposition choice;
- collocations;
- unnecessary nominalization;
- overly literal Chinese-English constructions;
- repetitive transitions.

### Pass 5 — Evidence calibration

Check every strong verb/adjective:

- significant;
- robust;
- validated;
- accurate;
- reliable;
- causal;
- critical;
- dominant;
- negligible;
- superior.

Each should have a clear basis.

### Pass 6 — Technical-integrity comparison

Compare original and revised text. Confirm that no protected element changed.

---

## 6. Introduction Checklist

A strong Introduction should normally make clear:

- the specific engineering/scientific problem;
- why it matters in the investigated context;
- the controlling mechanism or difficulty;
- what prior work establishes;
- the specific unresolved issue;
- what this study does;
- the actual contributions.

Warnings:

- generic urbanization/infrastructure/sustainability opening;
- one-paper-per-sentence literature catalogue;
- `few studies` as the entire gap;
- contribution statements that repeat the Methods section;
- novelty claims without technical differentiation.

---

## 7. Methods Checklist

### Field / Experimental

Check whether the manuscript makes clear:

- site/specimen source;
- geometry/dimensions;
- equipment/sensors where relevant;
- loading or construction sequence;
- sampling;
- preprocessing;
- repeatability/uncertainty when available;
- output quantity definitions.

### Numerical

Check:

- physical idealization;
- governing equations;
- constitutive model;
- geometry;
- discretization;
- boundary and initial conditions;
- parameter source;
- solver/time step;
- contact/interface;
- verification;
- validation.

### TBM Operational Data

Check:

- data source and time/chainage/ring reference;
- input vs response channels;
- derived indicators;
- aggregation window;
- missing/invalid data treatment;
- geology/label provenance.

---

## 8. Chinese → English Translation Workflow

### Step A — Recover technical logic

Before translating, identify:

- subject;
- action/relationship;
- quantity;
- condition;
- comparison;
- interpretation.

Chinese technical sentences often omit an explicit subject or combine several rhetorical functions. Recover the logic first.

### Step B — Protect terminology

Build a short local glossary for recurring terms. Use one English term consistently unless the manuscript deliberately distinguishes concepts.

### Step C — Translate function, not filler

Examples:

- `可以看出` → usually state the observation directly;
- `值得注意的是` → state the notable fact and why it matters;
- `具有重要工程意义` → specify the design/construction/monitoring implication;
- `验证了模型的正确性` → determine whether the evidence is verification, validation or simply agreement;
- `变化规律` → translate as the actual trend/evolution rather than `change law`.

### Step D — Rebuild sentence boundaries

Split long Chinese sentences when they contain:

- method + result + mechanism in one sentence;
- several unrelated coordinate clauses;
- multiple figure references;
- more than one contrast.

Do not split technical definitions that need to remain together.

### Step E — Final terminology and number check

Compare the translation with the Chinese source line by line for numbers, units, symbols and technical qualifiers.

---

## 9. Naturalness Check

Natural academic prose is a consequence of clear thought and section function, not deliberate imperfection.

Look for:

- repeated `This study...` openings;
- repeated claim→evidence→implication paragraph structure;
- excessive `Moreover/Furthermore/Additionally`;
- generic praise such as `excellent`, `remarkable`, `highly accurate`;
- symmetrical lists whose items could be integrated more naturally;
- repeated conclusion-like sentences at the end of every paragraph;
- overuse of hedging when results are actually direct measurements;
- overconfident mechanism language when evidence is only associative.

Do **not**:

- intentionally insert grammar errors;
- randomly vary sentence length to satisfy detector thresholds;
- add artificial uncertainty;
- optimize wording for GPTZero or another detector.

---

## 10. Results Checklist

For every Results subsection:

- Is the organizing variable clear — time, depth, chainage, ring, scenario, parameter, spatial location?
- Are key quantitative changes stated?
- Are figure/table references attached to specific observations?
- Is interpretation separated from raw observation where needed?
- Are unexpected results discussed rather than hidden?
- Are comparison baselines explicit?
- Are statistical claims supported by actual statistics?

Avoid narrating figures from left to right without extracting a research finding.

---

## 11. Discussion Checklist

A useful Discussion may answer:

- What mechanism best explains the main result?
- Which evidence supports that mechanism?
- Why does the result agree/disagree with previous studies?
- Which geological, scale, boundary or operational differences matter?
- What does the result imply for design, construction, monitoring or prediction?
- Under what conditions does that implication apply?

A limitation paragraph is optional. State boundaries where they materially affect interpretation.

---

## 12. Conclusion Checklist

Check that the Conclusion:

- answers the research questions;
- keeps quantitative findings exact;
- does not add new evidence;
- does not introduce new literature;
- does not strengthen claims beyond Results/Discussion;
- states engineering implications specifically;
- avoids re-listing contributions mechanically.

---

## 13. Full-Paper Audit

Audit in this order:

### A. Technical integrity

- numbers/units;
- notation;
- terminology;
- definitions;
- figure/table references;
- citations.

### B. Cross-section consistency

- same parameter names in Methods and Results;
- same contribution wording in Abstract/Introduction/Conclusion;
- no discrepancy in test/model conditions;
- consistent abbreviations.

### C. Evidence strength

- observational vs causal;
- verification vs validation;
- calibration vs independent test;
- case-specific vs general.

### D. Section logic

- introduction leads to method;
- method supports results;
- discussion interprets rather than repeats;
- conclusion traces to body.

### E. Language quality

- awkward translation;
- redundant scaffolding;
- collocation errors;
- overlong noun phrases;
- mechanical transitions;
- formulaic paragraph repetition.

---

## 14. High-Risk Technical Terms

Review these manually whenever they appear:

- validate / verify;
- significant;
- causal;
- failure;
- stability;
- convergence;
- accuracy;
- uncertainty;
- sensitivity;
- robustness;
- effective stress;
- penetration;
- thrust;
- torque;
- specific energy;
- FPI;
- rock class / rock mass class;
- warning level;
- strength class.

Their meaning is domain-specific and should not be changed by stylistic substitution.

---

## 15. Output Style

### Polishing / translation

Return the finished text first. Mention only important technical ambiguities or evidence-strength changes that need attention.

### Audit

Prioritize findings:

1. TECHNICAL
2. EVIDENCE
3. STRUCTURE
4. TERMINOLOGY
5. STYLE

Do not create artificial problems just to make the audit look comprehensive.

---

## 16. Journal-Specific Use

This skill provides a civil/tunnelling baseline. For a named target journal:

1. follow its current author guidelines;
2. inspect recent papers from the journal;
3. use the present skill for technical integrity, discipline language and paragraph logic;
4. adjust section length, heading style, abstract format and journal-specific conventions separately.

Do not claim this reference represents a journal statistically unless a real corpus analysis has been performed.
