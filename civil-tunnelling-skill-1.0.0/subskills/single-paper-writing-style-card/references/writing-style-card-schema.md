# WritingStyle.md Card Schema

Use this schema for the final single-paper writing-style card. The file name must be exactly `WritingStyle.md`.

The card describes the writing behavior observed in **one paper**. It must not be presented as the author's general style unless multiple papers have been analyzed separately.

## Front matter

```yaml
---
artifact: single-paper-writing-style-card
schema_version: "1.0"
scope: single-paper
source_item_key: "<Zotero parent item key>"
source_title: "<paper title>"
source_doi: "<DOI if available>"
source_year: "<year if available>"
source_language: "<language>"
source_fulltext: "ai-butler-mineru-cache | online-mineru"
source_attachment_title: "<cached MinerU attachment title, if used>"
generated_at: "<ISO-8601 timestamp>"
---
```

Do not put API keys, tokens, local secrets, temporary paths, or private service credentials in front matter.

## Required sections

# Writing Style Card

## 1. Scope and confidence

State that this is a single-paper profile. Record overall evidence quality and any extraction limitations. Use `high`, `medium`, or `low` confidence only when justified.

## 2. One-paragraph style fingerprint

Summarize the paper's most distinctive writing behavior in 5–8 concise observations. Focus on prose and rhetoric, not scientific findings.

## 3. Section-level rhetorical architecture

Use a table with columns:

| Section | Dominant rhetorical moves | Typical ordering | Confidence |
|---|---|---|---|

Cover only sections actually present in the paper, such as Abstract, Introduction, Methods, Results, Discussion, Conclusions, Engineering Background, Numerical Method, Validation, or Case Study.

## 4. Paragraph architecture

Describe recurring paragraph-level patterns, such as:

- context → specific problem → gap → present study;
- observation → quantitative evidence → comparison → interpretation;
- method purpose → implementation → parameter/detail → output;
- mechanism claim → evidence → boundary/qualification.

For each claimed pattern, distinguish repeated behavior from a one-off example.

## 5. Sentence architecture

Describe observable tendencies in:

- sentence length and variation;
- simple vs. multi-clause sentences;
- active/passive balance;
- preferred grammatical subjects;
- nominalization density;
- sentence-opening patterns;
- placement of conditions, qualifications, and causal clauses.

Prefer deterministic statistics when a code/runtime tool can compute them. Do not invent numeric averages or percentages from impression alone.

## 6. Lexical and collocational profile

Summarize recurring choices for:

- reporting verbs;
- change/trend verbs;
- comparison language;
- cause/mechanism language;
- method-description verbs;
- uncertainty/hedging;
- confidence/boosting;
- transition devices;
- discipline-specific collocations.

Do not create a generic academic phrase bank. Include only patterns supported by the source paper.

## 7. Evidence and claim calibration

Describe how the paper moves from data/results to interpretation:

- observation vs. interpretation;
- association vs. causation;
- numerical/experimental/field validation wording;
- strength of hedging;
- treatment of applicability boundaries;
- use of quantitative evidence.

## 8. Technical presentation style

Where applicable, describe:

- equations and symbol introduction;
- units and numerical values;
- figure/table references;
- parameter definitions;
- geological/material/machine terminology;
- experimental/numerical procedure sequencing;
- distinction between measured, derived, simulated, and interpreted quantities.

## 9. Citation and literature-synthesis style

Describe how prior work is grouped and compared, for example by author chronology, mechanism, method, agreement/disagreement, or research gap.

## 10. Cohesion and transitions

Describe paragraph-to-paragraph and sentence-to-sentence cohesion, including explicit connectors, lexical repetition, pronoun/reference use, and topic progression.

## 11. Reusable writing rules

Convert the strongest observations into 8–15 operational rules that can guide later drafting. Rules must be abstract enough to avoid copying source sentences.

Example form:

- `When reporting a trend, state the direction and quantitative evidence before the mechanism interpretation.`
- `Introduce numerical-model parameters only after the physical role of the parameter has been established.`

## 12. Section-specific imitation guide

For each major section actually present, provide a short reusable blueprint. Use rhetorical functions rather than source wording.

## 13. Applicability boundary

State what the card supports and what it does not support. In particular:

- one paper does not establish an author-wide style;
- paper-specific constraints may reflect the journal or study design;
- unusual wording observed once should not be elevated to a stable rule.

## 14. Evidence ledger

Use a compact table:

| Observation | Location/section | Evidence frequency | Confidence |
|---|---|---:|---|

The ledger should allow another agent to trace each important style rule back to the paper without reproducing long passages.

## Quotation rule

Prefer paraphrase and abstract patterns. If a micro-example is necessary, keep any verbatim quotation very short and use it only as evidence for a style observation. Never reproduce long paragraphs or substantial contiguous text from the source paper.
