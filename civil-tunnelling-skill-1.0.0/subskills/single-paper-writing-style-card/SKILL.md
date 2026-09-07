---
name: "single-paper-writing-style-card"
description: "Generate a reusable writing-style card for one user-specified Zotero paper. Resolve the item through Zotero MCP, prefer the cached MinerU Markdown saved by zotero-AI-Butler, fall back to user-specified online MinerU parsing when no cached result exists, analyze the paper's writing behavior, generate WritingStyle.md, and import it back as a child attachment of the original Zotero item. Triggers on: 单篇文献写作风格卡, 文献风格卡, Zotero写作风格, WritingStyle.md, single-paper style card."
metadata:
  version: "1.0.0"
  status: active
  task_type: tool-orchestrated-analysis
  parent_skill: "civil-tunnelling-writing-style-guide"
  dependencies:
    - "https://github.com/cookjohn/zotero-mcp"
    - "https://github.com/steven-jianhao-li/zotero-AI-Butler"
---

# Single-Paper Zotero Writing Style Card

Generate a writing-style profile from **one user-specified paper in the local Zotero library**, save the result as `WritingStyle.md`, and attach that file to the paper's original Zotero parent item.

This subskill adapts the parent repository's core distillation idea: observe real prose, separate recurrent patterns from isolated examples, organize them into reusable sentence/paragraph/rhetorical guidance, and preserve evidence boundaries. Here the corpus is one paper rather than a journal-scale paper set.

The output is a **single-paper style card**, not an author-wide style model.

---

## Dependencies and verified interfaces

### Zotero MCP

Dependency: `cookjohn/zotero-mcp`

Current expected semantic operations are:

- `search_library` — resolve a user-specified paper;
- `get_item_details` — obtain parent-item metadata and child attachments;
- `get_content` — read a specific attachment or item content;
- `write_item` with `action="import"` — import a local Markdown file as an attachment to an existing Zotero item.

At execution time, use the actual MCP tool schema exposed by the connected Zotero MCP server. Tool discovery/schema returned by the running server overrides names or parameters documented here if the upstream project changes.

For the final style-card import, prefer the equivalent of:

```text
write_item(
  action="import",
  filePath=<local path to WritingStyle.md>,
  parentItemKey=<original bibliographic parent item key>,
  title="WritingStyle.md",
  linkMode="imported_file",
  libraryID=<same library as source item>
)
```

Use `imported_file` when available so the card is copied into Zotero storage rather than remaining dependent on a temporary local path.

### zotero-AI-Butler MinerU cache

Dependency: `steven-jianhao-li/zotero-AI-Butler`

AI-Butler currently identifies its saved MinerU Markdown using these conventions:

- attachment title starts with `[AI-Butler] MinerU Markdown`;
- or attachment tag contains `AI-MinerU-Markdown`;
- compatibility fallback: attachment content type is `text/markdown` and its title contains `MinerU`.

Use these rules to detect the preferred full-text source before attempting a new MinerU parse.

---

# Trigger Conditions

Use this subskill when the user asks to:

- summarize the writing style of one Zotero paper;
- create a `WritingStyle.md` / writing-style card for a paper;
- analyze how a specified paper writes its Introduction, Methods, Results, Discussion, etc.;
- create a reusable style profile from one local Zotero item.

Typical triggers:

`单篇文献写作风格卡`, `文献风格卡`, `Zotero 写作风格`, `生成 WritingStyle.md`, `single-paper style card`, `paper writing-style profile`

Do not use this subskill for:

- multi-paper author-style synthesis;
- journal-wide corpus style extraction;
- ordinary manuscript polishing when no source paper is being profiled;
- scientific-content summarization without writing-style analysis.

---

# Required Input

The user must identify the target paper sufficiently to resolve it in Zotero. Accept, in descending precision:

1. Zotero item key;
2. DOI;
3. citation key;
4. exact or near-exact title;
5. title + author/year.

Do not ask the user to repeat metadata that Zotero MCP can resolve.

A MinerU parsing address/endpoint is optional at the start. Request it only when no readable AI-Butler MinerU Markdown attachment is available.

---

# HARD RULES

1. **The target is the original bibliographic parent item.** Do not attach `WritingStyle.md` to a PDF child attachment or to the MinerU Markdown child attachment.
2. **Prefer cached AI-Butler MinerU Markdown.** Do not call MinerU again when a valid readable AI-Butler MinerU Markdown attachment already exists.
3. **Do not silently fall back to Zotero's ordinary PDF text when the requested MinerU source is missing.** If no cached MinerU Markdown exists, follow the online-MinerU branch below.
4. **Do not claim one paper represents the author's general style.** Label all conclusions as single-paper observations.
5. **Do not invent style statistics.** Numeric sentence/paragraph statistics require deterministic counting or explicit evidence. Otherwise use qualitative descriptions.
6. **Do not turn scientific findings into style rules.** Separate what the paper says from how it says it.
7. **Do not copy long source passages.** Prefer paraphrased observations and abstract rhetorical templates.
8. **Do not expose credentials.** MinerU API keys/tokens must never appear in `WritingStyle.md`, logs intended for the user, or Zotero metadata.
9. **Do not silently create duplicate style cards.** Detect an existing `WritingStyle.md` child attachment before import and use the safest available update/replace path. If the installed MCP cannot replace an existing imported file, surface that constraint rather than silently accumulating duplicates.
10. **Verify the final attachment.** Re-read the Zotero parent item after import/update and confirm `WritingStyle.md` is attached to the intended item.

---

# End-to-End Workflow

## Step 0 — Preflight

Confirm that the connected Zotero MCP exposes the semantic capabilities needed to:

- search/read items;
- inspect attachments;
- read attachment content;
- import a local file as an attachment.

If an operation uses a renamed upstream tool, map by capability rather than failing on a hard-coded name.

## Step 1 — Resolve the target Zotero item

Use `search_library` unless the user already supplied an exact item key.

Then call `get_item_details` on the candidate item and verify:

- title;
- authors;
- year;
- DOI/citation key where available;
- library ID;
- item key;
- attachment list.

If the user selected a child attachment, resolve its parent bibliographic item and use the parent key for all later writes.

Only ask for disambiguation when multiple plausible Zotero items remain after metadata comparison.

## Step 2 — Inspect child attachments for AI-Butler MinerU Markdown

Search the target parent item's attachments in this order:

1. title starts with `[AI-Butler] MinerU Markdown`;
2. tag contains `AI-MinerU-Markdown`;
3. fallback: `text/markdown` attachment whose title contains `MinerU`.

If several candidates match, prefer the exact AI-Butler title/tag match and then the most recently modified valid attachment when modification metadata is available.

Record the selected attachment title/key for provenance.

## Step 3A — Cached MinerU branch

If a matching attachment exists:

1. read that specific Markdown attachment with `get_content` or the equivalent MCP content operation;
2. request complete/untruncated content when the MCP exposes a mode/content-control option;
3. verify that the result contains substantial article text rather than only metadata or a stub;
4. use this Markdown as the analysis source;
5. set `source_fulltext: ai-butler-mineru-cache` in the final card.

If the attachment is detected but cannot be read, report it as **cached-but-unreadable**. Do not pretend the cache is absent.

## Step 3B — Online MinerU fallback

Enter this branch only when no readable AI-Butler MinerU Markdown is available.

If the user has not already supplied a MinerU parsing address/endpoint, request it at this point.

Then:

1. identify the source PDF attachment belonging to the target parent item;
2. obtain the local PDF file or a tool-accessible file reference through the connected environment;
3. inspect the user-supplied MinerU endpoint/API contract before sending the file;
4. upload/submit the PDF according to that endpoint's actual contract;
5. poll or wait for the parsing job only through supported synchronous/tool mechanisms;
6. retrieve the finished MinerU result;
7. extract the primary Markdown full text;
8. validate that the Markdown corresponds to the target paper;
9. set `source_fulltext: online-mineru` in the final card.

Do not assume the official MinerU v4 request schema for an arbitrary user-supplied URL. Verify the endpoint contract first.

If authentication is required, obtain credentials through the execution environment's secure mechanism. Never write credentials into the style card.

The required final side effect of this subskill is `WritingStyle.md`. Do not label an independently parsed Markdown file as an AI-Butler attachment unless AI-Butler itself created it or the user explicitly requests that additional action.

## Step 4 — Build the analysis corpus

Preserve section boundaries from the MinerU Markdown.

Separate material into:

- prose body;
- headings;
- equations/math blocks;
- tables;
- figure/table captions;
- reference list/bibliography;
- front matter/affiliations;
- acknowledgements/supplementary boilerplate.

Use the **prose body** as the primary style-analysis corpus. Exclude the bibliography, author affiliations, publisher boilerplate, and other non-authorial material from sentence/paragraph style statistics.

Retain captions, equations, figures/tables references, and technical objects as secondary evidence for the paper's technical-presentation style.

## Step 5 — Segment by rhetorical section

Map actual headings to functional sections, for example:

- Abstract;
- Introduction;
- Literature Review;
- Engineering/Site Background;
- Methods / Experimental Program;
- Numerical Method;
- Validation / Verification;
- Results;
- Discussion;
- Conclusions.

Do not force every paper into the same IMRaD structure. If a section is absent, omit it from the card.

## Step 6 — Analyze writing behavior

Analyze at least these dimensions:

### A. Macro/rhetorical architecture

- ordering of section-level moves;
- how context becomes a research question;
- how methods are introduced;
- how results move into interpretation;
- how conclusions synthesize claims.

### B. Paragraph architecture

Identify repeated paragraph structures and distinguish recurring patterns from isolated examples.

### C. Sentence architecture

Assess:

- sentence-length distribution/variation;
- clause complexity;
- active/passive usage;
- grammatical subjects;
- nominalization;
- sentence openings;
- placement of conditions and qualifications.

When a scripting/runtime tool is available, compute simple deterministic statistics such as sentence count, median sentence length, interquartile range, and paragraph sentence counts. If not available, omit numeric claims rather than estimating them.

### D. Lexical/collocational behavior

Extract recurring functional language for:

- reporting;
- trends and comparison;
- mechanism/causality;
- methods;
- validation;
- uncertainty;
- transitions;
- engineering terminology.

### E. Evidence calibration

Determine how the paper differentiates:

- result vs. interpretation;
- association vs. causation;
- measured vs. derived vs. simulated quantities;
- verified numerical behavior vs. physical validation;
- local findings vs. broader applicability.

### F. Technical presentation

For civil/tunnelling papers, inspect how the paper presents:

- geological/material conditions;
- machine/test/model parameters;
- equations, symbols, and units;
- numerical setup;
- figures and tables;
- uncertainty/quality control;
- TBM/shield/EPB operational quantities where relevant.

### G. Citation and cohesion behavior

Inspect how prior studies are grouped and how paragraphs/sentences connect.

## Step 7 — Calibrate evidence strength

Use evidence frequency to prevent overgeneralization:

- **High confidence** — clearly repeated across multiple sections/instances;
- **Medium confidence** — repeated in a narrower section or supported by several examples;
- **Low confidence** — observed once or dependent on uncertain section parsing.

Never turn a one-off phrase into a stable style rule without labeling it as low confidence.

## Step 8 — Generate `WritingStyle.md`

Load `references/writing-style-card-schema.md` and follow it exactly enough that downstream agents can parse the card consistently.

The final card must emphasize reusable writing behavior rather than content summary.

Required filename:

```text
WritingStyle.md
```

Write the file as UTF-8 Markdown to a stable local temporary/work path accessible to Zotero MCP's import operation.

## Step 9 — Validate before Zotero import

Check that:

- filename is exactly `WritingStyle.md`;
- source item key/title are correct;
- source provenance is recorded;
- no API key/token is present;
- no author-wide generalization is made from one paper;
- no unsupported numeric style metrics are present;
- no substantial source text has been copied;
- the card contains actionable writing rules and an evidence ledger.

## Step 10 — Handle an existing style-card attachment

Before importing, inspect the parent item for an existing child attachment whose filename/title resolves to `WritingStyle.md`.

Preferred behavior:

1. update/replace the existing file through the installed Zotero MCP if a safe supported operation exists;
2. otherwise use an available writable local attachment path only when the execution environment can verify it is the existing attachment's file;
3. if neither replacement path is supported, do not silently create a duplicate — tell the user that the installed MCP version cannot atomically replace the existing attachment and require an explicit duplicate/cleanup decision.

## Step 11 — Import into the original Zotero item

When no existing card needs replacement, import the generated file as a child attachment of the **original bibliographic parent item**.

Prefer:

```text
action = import
parentItemKey = <original parent key>
title = WritingStyle.md
linkMode = imported_file
libraryID = <source item's library>
```

Do not attach it to the MinerU Markdown attachment.

## Step 12 — Verify the write

Call `get_item_details` again on the original parent item and confirm:

- `WritingStyle.md` appears as a child attachment;
- it belongs to the intended parent item;
- only one active style-card attachment is present unless the user explicitly requested versions.

Report completion with the source paper title/item key and the verified attachment name.

---

# Output Card Design

The detailed schema lives in:

`references/writing-style-card-schema.md`

The card must include:

1. scope/confidence;
2. one-paragraph style fingerprint;
3. section-level rhetorical architecture;
4. paragraph architecture;
5. sentence architecture;
6. lexical/collocational profile;
7. evidence and claim calibration;
8. technical presentation style;
9. citation/literature-synthesis style;
10. cohesion/transitions;
11. reusable writing rules;
12. section-specific imitation guide;
13. applicability boundary;
14. evidence ledger.

---

# Relationship to the Parent Writing Skill

This subskill produces a **paper-specific style reference artifact**. Later writing/polishing tasks may load `WritingStyle.md` alongside the parent civil/tunnelling references.

Priority during later imitation:

1. technical truth and the user's manuscript facts;
2. explicit journal/manuscript requirements;
3. high-confidence rules from the selected paper's `WritingStyle.md`;
4. general civil/tunnelling writing references from the parent skill.

A paper-specific card can override generic stylistic preferences when there is no technical or journal conflict, but it can never override factual integrity, units, equations, citations, or evidence boundaries.
