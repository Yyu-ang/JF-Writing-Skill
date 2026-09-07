---
name: "civil-tunnelling-writing-style-guide"
description: "Academic writing reference for civil engineering, geotechnical engineering, tunnelling and underground-space research. Supports polishing, Chinese-to-English technical translation, paragraph restructuring and full-paper style audits. Triggers on: 隧道写作, 土木写作, 岩土写作, CTE-skill, tunnelling polish, geotechnical translate."
metadata:
  version: "1.0.0"
  status: active
  task_type: open-ended
  upstream_architecture: "Ryyyyyyy233/JF-Writing-Skill"
---

# Civil & Tunnelling Engineering Writing Style Guide v1.0

A modular reference for drafting, translating and polishing academic prose in civil engineering, geotechnical engineering, tunnelling and underground-space research.

The architecture is adapted from `Ryyyyyyy233/JF-Writing-Skill`: diagnose the task, load only the relevant references, apply patterns selectively, then perform a technical-integrity check.

This skill is **not** a dynamic journal-corpus learner. It does not claim that its patterns were statistically extracted from a specific tunnelling journal.

---

## Quick Start

```text
隧道写作：润色这段 TUST 引言
岩土写作：把这段中文试验结果翻译成英文
CTE-skill polish this numerical-method section
geotechnical translate this discussion paragraph
```

Execution flow:

1. **Diagnose** — identify section, research method and requested operation.
2. **Load references** — use only the modules needed for the task.
3. **Protect technical content** — lock facts, units, symbols, equations, citations and numerical values.
4. **Apply patterns** — improve structure, wording, evidence calibration and engineering logic.
5. **Verify** — check technical integrity, terminology and evidence boundaries.

---

## Trigger Conditions

### Chinese

`隧道写作`, `土木写作`, `岩土写作`, `隧道润色`, `岩土润色`, `隧道翻译`, `土木论文`, `CTE-skill`

### English

`CTE-skill`, `tunnelling polish`, `tunnel writing`, `geotechnical writing`, `geotechnical translate`, `civil engineering polish`

### Do not automatically use for

- legal/business/general-purpose writing;
- unrelated humanities or finance writing;
- code review without manuscript prose;
- requests that only ask for factual engineering analysis rather than writing help.

---

## Mode Selection

| User need | Mode | Main references |
|---|---|---|
| Polish Introduction | Introduction polish | `sentence-templates.md`, `paragraph-patterns.md` |
| Polish Methods | Method polish | `sentence-templates.md`, `meta-discourse.md` |
| Polish Results | Results polish | `paragraph-patterns.md`, `phrase-bank.md` |
| Polish Discussion | Discussion polish | `paragraph-patterns.md`, `meta-discourse.md` |
| Chinese → English | Technical translation | `phrase-bank.md`, `usage-guide.md` |
| Restructure paragraph | Paragraph restructure | `paragraph-patterns.md` |
| Improve abstract/conclusion | Synthesis polish | `sentence-templates.md`, `usage-guide.md` |
| Full-paper audit | Full audit | all five reference files |
| Check numerical/experimental credibility wording | Evidence-boundary audit | `meta-discourse.md`, `usage-guide.md` |

---

## Research-Method Classification

Before polishing, classify the manuscript as one or more of:

1. field monitoring / case history;
2. laboratory test / physical model test;
3. engineering geology / site investigation;
4. analytical / theoretical;
5. numerical simulation / computational mechanics;
6. constitutive modelling;
7. TBM / shield / EPB operational-data study;
8. data-driven / machine learning for civil or tunnelling engineering;
9. review / synthesis;
10. mixed method.

The method class changes what must be preserved and what evidence language is appropriate.

---

# HARD TECHNICAL RULES

These override all stylistic preferences.

1. **Never invent technical content.** Do not add data, results, citations, geological conditions, equipment specifications, machine parameters, support parameters, boundary conditions, material properties, monitoring locations or validation outcomes.
2. **Preserve numerical values and units.** Do not round, convert or reinterpret values unless the user explicitly requests it.
3. **Preserve equations and notation.** Keep equation content, LaTeX commands, symbols, subscripts, superscripts and author-defined variables unchanged unless editing mathematics is explicitly requested.
4. **Preserve citations and cross-references.** Do not create, delete or replace references, figure/table labels or equation numbers during language polishing.
5. **Preserve engineering definitions.** Do not silently merge quantities such as total thrust, main thrust and auxiliary thrust; measured penetration and derived penetration index; raw and filtered signals; nominal and effective stress.
6. **Keep provenance visible.** Distinguish measured/input quantities, derived quantities, numerical outputs, interpreted mechanisms and human-entered labels.
7. **Do not upgrade evidence strength.** Correlation is not causation; numerical agreement is not automatically physical validation; sensitivity is not uncertainty quantification unless the study supports that claim.
8. **Keep scope bounded.** A single tunnel, soil type, rock mass, test condition or numerical benchmark does not automatically justify universal statements.
9. **Do not convert discipline-specific prose into generic ML/CS prose.** When machine learning is used, the engineering problem and data provenance remain primary.
10. **Do not optimize for AI detectors.** Improve naturalness through argument quality, specificity and non-mechanical structure rather than artificial randomness or detector-targeted tricks.

---

# Reference Files Index

| File | Content | Load when |
|---|---|---|
| `references/sentence-templates.md` | Section-specific sentence functions for introductions, methods, validation, results, discussion and conclusions | sentence-level drafting/polishing |
| `references/phrase-bank.md` | engineering collocations, reporting verbs, comparison language, hedging, validation language, numerical and field terminology | translation and wording |
| `references/paragraph-patterns.md` | reusable paragraph architectures for engineering papers | restructuring paragraphs or sections |
| `references/meta-discourse.md` | interpretation control, validity boundaries, data/model distinctions, limitations and layered analysis | careful discussion/validation wording |
| `references/usage-guide.md` | end-to-end workflow and quality-control checklists | translation, full-paper audit, final pass |

---

# Core Workflow

## Step 1 — Diagnose context

Determine:

- manuscript section;
- user goal: polish / translate / draft / restructure / audit;
- research method class;
- engineering object: tunnel, lining, rock mass, soil, support, TBM, shield, excavation, slope, foundation, etc.;
- whether the text contains equations, units, citations or numerical results that must be locked.

Do not ask questions that can be inferred from the provided section.

## Step 2 — Load relevant references

Most paragraph-level tasks need only 1–2 reference files. Do not load every module mechanically.

## Step 3 — Identify rhetorical function

For each paragraph, identify its main function, for example:

- establish engineering context;
- define a mechanism;
- identify a literature gap;
- state contribution;
- describe site/geology;
- explain experimental setup;
- explain numerical formulation;
- validate a model;
- report a trend;
- compare scenarios;
- explain mechanism;
- state applicability boundary.

## Step 4 — Apply patterns selectively

Use patterns as references. Do not force every paragraph into claim → evidence → implication. Technical sections often require asymmetric or multi-stage structures.

## Step 5 — Calibrate claim strength

Use wording that matches evidence:

- observation: `X increased from ... to ...`;
- association: `X was associated with Y`;
- suggestive mechanism: `the pattern is consistent with ...`;
- supported mechanism: `the combined evidence indicates that ...`;
- verified numerical property: describe the actual verification test;
- validated physical behavior: identify the independent experiment/field benchmark.

Avoid replacing cautious author language with stronger causal or universal claims.

## Step 6 — Technical-integrity verification

Before returning polished text, check:

- all numbers preserved;
- all units preserved;
- equations and symbols preserved;
- citations and cross-references preserved;
- technical terms remain consistent;
- geological/machine/material/test facts unchanged;
- no new claim, mechanism or recommendation introduced.

---

# Section Guidance

## Abstract

A strong engineering abstract commonly contains:

problem/context → unresolved issue → method/data → principal result → mechanism or engineering implication.

Prefer the actual engineering object over generic infrastructure claims. Use quantitative results when already present in the manuscript.

## Introduction

Common useful progression:

engineering/scientific problem → relevant mechanism → what existing approaches establish → unresolved limitation/gap → present study → concrete contributions.

Avoid opening with broad claims such as rapid urbanization, increasing infrastructure demand or general sustainability importance unless they are directly necessary for the paper.

## Literature Review

Organize by mechanism, engineering question, method or unresolved issue rather than by author chronology. Compare what approaches can and cannot resolve for the present problem.

## Site / Geology / Engineering Background

Include details needed to interpret the study:

- tunnel geometry and depth/overburden;
- geological units and rock/soil properties;
- groundwater;
- discontinuities/faults/weak zones;
- in-situ stress when relevant;
- excavation method;
- support/lining;
- TBM/shield/EPB configuration when relevant.

Do not bury the research question under project history.

## Experimental / Field Methods

Make traceable:

specimen/site → instrumentation → procedure → loading/construction sequence → acquisition/sampling → preprocessing → derived quantities → uncertainty/quality control.

Do not invent missing instrument accuracy or calibration details.

## Numerical / Computational Methods

Where relevant, make traceable:

physical problem → governing equations → constitutive model → geometry → discretization → initial/boundary conditions → parameters → solver/time step → contact/interface → verification/validation → outputs.

Distinguish verification from validation.

## TBM / Shield / EPB Studies

Keep separate:

1. geological/ground conditions;
2. machine configuration;
3. operator/control inputs;
4. measured machine response;
5. derived performance indicators;
6. interpreted/human-entered labels.

Preserve exact definitions of thrust, torque, penetration, advance rate, chamber pressure, specific energy, FPI-type indicators and auxiliary-system quantities.

## Data-Driven Engineering

Keep the engineering problem central. Preserve:

- data provenance;
- unit of observation;
- train/validation/test split;
- leakage prevention;
- feature definitions;
- target/label provenance;
- missing-data treatment;
- baseline models;
- metrics;
- uncertainty/generalization boundary;
- engineering interpretation.

## Results

Prefer:

observation/result → quantitative evidence → comparison → mechanism/interpretation when supported.

Do not simply narrate every figure. Extract the engineering meaning.

## Discussion

Use Discussion to explain mechanisms, compare evidence, reconcile discrepancies and define applicability. Engineering recommendations must remain within tested or observed conditions.

## Conclusion

Synthesize findings in the order of the research questions. Preserve quantitative findings. Do not introduce new literature, new results or new mechanisms.

---

# Naturalness and Anti-Formulaic Audit

The goal is clear professional prose, not deliberate irregularity.

Check whether:

1. multiple consecutive paragraphs use exactly the same rhetorical skeleton;
2. every transition is made explicit with `Moreover/Furthermore/Additionally`;
3. generic evaluation words replace quantitative evidence;
4. contribution claims are inflated relative to the actual work;
5. paragraph openings repeat the same `This study... / The results... / It can be seen...` form;
6. caveats are added mechanically rather than because the evidence requires them;
7. sentence length varies naturally with technical content rather than by an artificial target;
8. terminology remains stable across sections.

Do not degrade grammar, insert uncertainty, or randomize structure merely to appear human.

---

# Translation Rules: Chinese → English

Translate rhetorical function and technical meaning rather than word order.

Priorities:

1. preserve technical content;
2. identify subject and causal/associational relation;
3. remove redundant Chinese discourse scaffolding;
4. choose standard engineering collocations from `phrase-bank.md`;
5. split overloaded Chinese sentences when English logic requires it;
6. retain necessary qualifications and scope boundaries;
7. perform the technical-integrity check.

Avoid automatic mappings such as:

- `可以看出` → always `It can be seen that`;
- `值得注意的是` → always `It is worth noting that`;
- `具有重要意义` → always `is of great significance`.

Translate the actual function instead.

---

# Output Behavior

For polishing/translation, provide the finished revised text first. Add a concise note only when a change in logic, terminology or evidence strength needs user attention.

For audits, report issues by priority:

- **TECHNICAL** — possible factual/definition/units/evidence problem;
- **STRUCTURE** — paragraph or section logic;
- **TERMINOLOGY** — inconsistent engineering terms;
- **EVIDENCE** — claim stronger than support;
- **STYLE** — clarity, repetition, awkward translation or formulaic prose.

Do not manufacture issues simply to fill every category.
