# Civil & Tunnelling Engineering Writing Skill

A modular academic-writing skill for **civil engineering, geotechnical engineering, tunnelling and underground-space engineering**.

This repository is adapted from the architecture of [`Ryyyyyyy233/JF-Writing-Skill`](https://github.com/Ryyyyyyy233/JF-Writing-Skill). It keeps the upstream design pattern — a lightweight `SKILL.md` orchestrator plus on-demand reference modules for sentence patterns, phrase choices, paragraph structures, meta-discourse and a polishing workflow — while replacing the Journal of Finance / financial-economics content with civil- and tunnelling-engineering guidance.

## Scope

The skill is designed for papers involving:

- civil and geotechnical engineering;
- tunnelling and underground construction;
- rock mechanics and engineering geology;
- TBM, shield and EPB tunnelling;
- field monitoring and engineering case histories;
- laboratory and physical-model tests;
- FEM/FDM/DEM/MPM and other numerical methods;
- constitutive modelling and computational mechanics;
- data-driven / machine-learning methods used for civil and tunnelling problems.

## Architecture

```text
civil-tunnelling-skill-1.0.0/
├── SKILL.md
├── README-chinese.md
├── README-english.md
└── references/
    ├── sentence-templates.md
    ├── phrase-bank.md
    ├── paragraph-patterns.md
    ├── meta-discourse.md
    └── usage-guide.md
```

The main skill diagnoses the section, research method and requested task, then loads only the relevant references. This mirrors the modular structure of the upstream JF skill while changing the professional content.

## Typical tasks

| Request | Main modules |
|---|---|
| Polish an Introduction | `sentence-templates.md` + `paragraph-patterns.md` |
| Translate Chinese technical prose into academic English | `phrase-bank.md` + `usage-guide.md` |
| Polish Methods for numerical simulation | `sentence-templates.md` + `meta-discourse.md` |
| Improve Results/Discussion | `paragraph-patterns.md` + `meta-discourse.md` |
| Audit a full paper | all five references |
| Check terminology, units and evidence boundaries | `usage-guide.md` + `meta-discourse.md` |

## Core principles

1. **Technical truth outranks style.** Do not change equations, variables, units, numerical results, citations, geological conditions, machine parameters, boundary conditions or experimental facts for stylistic reasons.
2. **Engineering evidence must remain traceable.** Distinguish measurement, input, derived quantity, numerical output, interpretation and human-entered labels.
3. **Mechanistic writing is preferred to generic significance claims.** Describe what changes, by how much, under what conditions, and why the evidence supports the interpretation.
4. **Do not turn civil papers into generic CS/ML papers.** Data-driven methods remain subordinate to the engineering problem, data provenance and deployment boundary.
5. **Naturalness is checked by clarity and variation, not detector-gaming rules.** The fixed AI-detector-oriented thresholds and deliberate sentence-length randomization from the original JF skill are not carried into this adaptation.
6. **Patterns are references, not compulsory templates.** Use only the structures that fit the actual argument and evidence.

## Important limitation

The original JF repository reports patterns extracted from a large Journal of Finance corpus. This civil/tunnelling adaptation does **not** claim an equivalent journal-frequency corpus. Its engineering patterns are a discipline-oriented writing reference. If a manuscript targets a specific journal, its author guidelines and actual published papers should still be consulted.

## Suggested triggers

- `隧道写作`
- `土木写作`
- `岩土写作`
- `CTE-skill`
- `tunnelling polish`
- `geotechnical translate`

## License and attribution

The upstream repository is MIT licensed. This adaptation retains the existing MIT license and repository history. Architecture attribution: `Ryyyyyyy233/JF-Writing-Skill`.
