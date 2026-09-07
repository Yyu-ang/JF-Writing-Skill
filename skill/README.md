# journal-adapt-tunnelling skill

This folder contains the executable instructions for a civil/geotechnical/
tunnelling adaptation of journal-adapt.

## Inputs

The skill asks for:

1. target journal or writing destination;
2. primary corpus (normally target-journal papers);
3. optional secondary corpus (high-quality topic/method-similar papers);
4. optional user / lab / advisor exemplars;
5. manuscript discipline and method type;
6. manuscript file;
7. sections to revise.

Preferred corpus size:

- primary target-journal corpus: 5–10 papers;
- secondary topic/method corpus: 2–6 papers;
- user/lab exemplars: 1–5 papers.

Markdown or clean text is preferred. PDFs require reliable conversion before
style analysis.

## Included civil/tunnelling base rules

```text
base_rules/
├── civil_tunnelling_engineering.md
├── geotechnical_experimental_field.md
└── computational_mechanics_numerical.md
```

The main rule file is always
`civil_tunnelling_engineering.md`.

Load one method-specific supplement when appropriate:

- laboratory / field / monitoring / case-history work:
  `geotechnical_experimental_field.md`
- numerical / computational mechanics / constitutive modelling:
  `computational_mechanics_numerical.md`

A TBM paper may use the field supplement, the numerical supplement, or both,
depending on its actual methods.

## Outputs

```text
[manuscript_name]_revised/
├── dynamic_writing_skill.md
├── style_profile.md
├── [section]_revised.md
├── [section]_revision_log.md
└── revision_summary.md
```

The dynamic skill must be reviewed before revision begins.
