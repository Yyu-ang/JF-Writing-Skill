# Civil & Tunnelling Engineering Writing Skill

A modular academic-writing skill for **civil engineering, geotechnical engineering, tunnelling and underground-space engineering**.

This repository is adapted from the architecture of [`Ryyyyyyy233/JF-Writing-Skill`](https://github.com/Ryyyyyyy233/JF-Writing-Skill). It keeps the upstream design pattern — a lightweight `SKILL.md` orchestrator plus on-demand reference modules for sentence patterns, phrase choices, paragraph structures, meta-discourse and a polishing workflow — while replacing the Journal of Finance / financial-economics content with civil- and tunnelling-engineering guidance.

The repository also includes a Zotero-oriented subskill that can distill the writing behavior of **one user-selected paper** into a reusable `WritingStyle.md` card and attach it back to the original Zotero item.

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
├── references/
│   ├── sentence-templates.md
│   ├── phrase-bank.md
│   ├── paragraph-patterns.md
│   ├── meta-discourse.md
│   └── usage-guide.md
└── subskills/
    └── single-paper-writing-style-card/
        ├── SKILL.md
        └── references/
            └── writing-style-card-schema.md
```

The main skill diagnoses the section, research method and requested task, then loads only the relevant references. A request to generate a style card for a Zotero paper is routed to the dedicated subskill instead of the generic polishing workflow.

## Typical tasks

| Request | Main modules |
|---|---|
| Generate `WritingStyle.md` for one Zotero paper | `subskills/single-paper-writing-style-card/SKILL.md` |
| Polish an Introduction | `sentence-templates.md` + `paragraph-patterns.md` |
| Translate Chinese technical prose into academic English | `phrase-bank.md` + `usage-guide.md` |
| Polish Methods for numerical simulation | `sentence-templates.md` + `meta-discourse.md` |
| Improve Results/Discussion | `paragraph-patterns.md` + `meta-discourse.md` |
| Audit a full paper | all five references |
| Check terminology, units and evidence boundaries | `usage-guide.md` + `meta-discourse.md` |

## Single-paper Zotero writing-style card

Typical request:

```text
单篇文献写作风格卡：分析我 Zotero 里的 <论文标题/DOI/citation key>，生成 WritingStyle.md 并挂回原文献条目。
```

The subskill follows this source priority:

```text
user-selected Zotero parent item
        ↓
inspect child attachments
        ↓
[AI-Butler] MinerU Markdown cache available?
   ├─ yes → read cached Markdown through Zotero MCP
   └─ no  → request the user's MinerU parsing endpoint and parse online
        ↓
analyze single-paper rhetorical / paragraph / sentence / lexical style
        ↓
generate UTF-8 WritingStyle.md
        ↓
import as a child attachment of the original Zotero bibliographic item
        ↓
re-read the item and verify the attachment
```

The workflow depends on:

- [`cookjohn/zotero-mcp`](https://github.com/cookjohn/zotero-mcp) for local Zotero search, item/attachment reading and attachment import;
- [`steven-jianhao-li/zotero-AI-Butler`](https://github.com/steven-jianhao-li/zotero-AI-Butler) for the cached MinerU Markdown attachment convention.

AI-Butler MinerU cache detection follows the plugin's current conventions: attachment titles beginning with `[AI-Butler] MinerU Markdown`, the `AI-MinerU-Markdown` tag, or a compatible `text/markdown` MinerU attachment.

The style card is intentionally scoped to **one paper**. It records section-level rhetoric, paragraph and sentence architecture, collocations, evidence calibration, technical-presentation behavior, cohesion, reusable writing rules and a traceable evidence ledger. It does not claim to represent the author's overall style.

## Core principles

1. **Technical truth outranks style.** Do not change equations, variables, units, numerical results, citations, geological conditions, machine parameters, boundary conditions or experimental facts for stylistic reasons.
2. **Engineering evidence must remain traceable.** Distinguish measurement, input, derived quantity, numerical output, interpretation and human-entered labels.
3. **Mechanistic writing is preferred to generic significance claims.** Describe what changes, by how much, under what conditions, and why the evidence supports the interpretation.
4. **Do not turn civil papers into generic CS/ML papers.** Data-driven methods remain subordinate to the engineering problem, data provenance and deployment boundary.
5. **Naturalness is checked by clarity and variation, not detector-gaming rules.** The fixed AI-detector-oriented thresholds and deliberate sentence-length randomization from the original JF skill are not carried into this adaptation.
6. **Patterns are references, not compulsory templates.** Use only the structures that fit the actual argument and evidence.
7. **Single-paper style evidence stays single-paper evidence.** A `WritingStyle.md` generated from one paper must not be presented as an author-wide or journal-wide writing model.

## Important limitation

The original JF repository reports patterns extracted from a large Journal of Finance corpus. This civil/tunnelling adaptation does **not** claim an equivalent journal-frequency corpus. Its engineering patterns are a discipline-oriented writing reference. If a manuscript targets a specific journal, its author guidelines and actual published papers should still be consulted.

The Zotero style-card subskill performs source-specific distillation only for the paper selected by the user. Broader author-style or journal-style claims require a separate multi-paper corpus workflow.

## Suggested triggers

- `隧道写作`
- `土木写作`
- `岩土写作`
- `CTE-skill`
- `单篇文献写作风格卡`
- `文献风格卡`
- `Zotero写作风格`
- `WritingStyle.md`
- `tunnelling polish`
- `geotechnical translate`

## License and attribution

The upstream repository is MIT licensed. This adaptation retains the existing MIT license and repository history. Architecture attribution: `Ryyyyyyy233/JF-Writing-Skill`.

Zotero workflow dependencies are separate upstream projects and remain under their own licenses:

- `cookjohn/zotero-mcp`
- `steven-jianhao-li/zotero-AI-Butler`
