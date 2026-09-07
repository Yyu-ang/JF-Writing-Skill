# journal-adapt-tunnelling

A corpus-grounded academic writing skill for **civil engineering, geotechnical engineering, tunnelling and underground-space research**.

This adaptation keeps the strongest workflow idea from [`WantongC/journal-adapt-writing-skill`](https://github.com/WantongC/journal-adapt-writing-skill):

> reference papers → per-paper Style Cards → corpus Style Profile → reviewable dynamic writing skill → section-by-section revision

It replaces generic CS/software-oriented engineering defaults with analysis and writing rules for:

- civil and geotechnical engineering;
- tunnelling and underground space;
- rock mechanics and engineering geology;
- TBM / EPB / shield tunnelling;
- field monitoring and engineering case histories;
- laboratory and physical model tests;
- numerical simulation and computational mechanics;
- constitutive modelling, FEM/FDM/DEM/MPM and coupled methods;
- data-driven / ML methods used inside civil and tunnelling research.

## Typical target journals

The workflow is corpus-driven and does not hard-code any venue. Typical writing destinations include:

- *Tunnelling and Underground Space Technology*;
- *Computers and Geotechnics*;
- *International Journal of Rock Mechanics and Mining Sciences*;
- *Rock Mechanics and Rock Engineering*;
- *Engineering Geology*;
- *Underground Space*;
- *Transportation Geotechnics*;
- other civil/geotechnical/tunnelling journals selected by the user.

## How it works

```text
Target-journal papers + topic/method papers + optional author/lab exemplars
                              ↓
                     Paper Style Cards
                              ↓
                       Style Profile
                              ↓
                 dynamic_writing_skill.md
                              ↓
                       Human review
                              ↓
                 Section-by-section revision
                              ↓
                     Technical integrity check
```

The dynamic skill is generated from the actual reference corpus. The bundled professional rules are fallbacks, not substitutes for target-journal evidence.

## Professional base rules

```text
skill/base_rules/
├── civil_tunnelling_engineering.md
├── geotechnical_experimental_field.md
└── computational_mechanics_numerical.md
```

`civil_tunnelling_engineering.md` is always loaded.

The field/experimental supplement is used for laboratory tests, monitoring, site investigation, TBM operational data and case histories. The numerical supplement is used for FEM/FDM/DEM/MPM, constitutive models, multiphysics and computational-mechanics papers. Mixed-method papers may load both.

## Civil/tunnelling Style Card dimensions

In addition to abstract, introduction, literature review, results and discussion, the skill can learn how a target corpus handles:

- engineering problem definition;
- geological and site conditions;
- construction, machine and support context;
- laboratory / field instrumentation;
- raw vs processed measurements and derived labels;
- governing equations and constitutive models;
- geometry, mesh/particles, boundary and initial conditions;
- parameter provenance and units;
- verification, validation and benchmarks;
- convergence, sensitivity, stability and conservation checks;
- engineering applicability and evidence-bounded interpretation.

## Install

For Claude Code:

```bash
mkdir -p ~/.claude/skills/journal-adapt-tunnelling
cp -R skill/* ~/.claude/skills/journal-adapt-tunnelling/
```

For Codex, install or symlink the `skill/` directory into your custom skills directory when supported, or keep this repository open and ask Codex to follow `skill/SKILL.md`.

## Invoke

```text
/journal-adapt-tunnelling
```

Example:

```text
Build a dynamic writing skill for a TUST manuscript using 8 target-journal papers,
4 topic-similar tunnelling papers, and 3 published papers from my research group.
The manuscript is a mixed TBM field-data and numerical study.
```

## Design principles

1. **Technical truth has highest priority.** Numerical values, units, equations, notation, citations, geological conditions, machine/support parameters and test/model facts are preserved unless the user explicitly authorizes a technical edit.
2. **Target-journal evidence outranks generic writing advice.** Recurring patterns in the reviewed primary corpus drive section structure and rhetorical choices.
3. **Civil/tunnelling context stays primary.** A data-driven tunnel paper is not automatically rewritten as a generic ML paper.
4. **No blanket anti-AI phrase blacklist.** A phrase is changed because it is empty, repetitive or inconsistent with the corpus—not because it appears on a generic list.
5. **Reference papers teach structure, not sentences.** Corpus prose is not quoted or paraphrased into the manuscript.
6. **Verification and validation stay distinct.** Numerical correctness and physical credibility are treated separately where relevant.

## Repository provenance

This repository currently contains the civil/tunnelling adaptation described above. Its Git history originates from the previously forked `JF-Writing-Skill` repository; the former finance-specific skill files have been removed from the current tree to avoid mixing unrelated writing systems.

The dynamic journal-adaptation architecture is inspired by and adapted from [`WantongC/journal-adapt-writing-skill`](https://github.com/WantongC/journal-adapt-writing-skill). See `docs/CIVIL_TUNNELLING_ADAPTATION.md` for the professional design rationale.

## License

MIT. See `LICENSE`.
