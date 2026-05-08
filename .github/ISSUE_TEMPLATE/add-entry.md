---
name: Add new entry
about: Propose a new ML eval claim for the Index.
title: "[entry] <model> — <benchmark>"
labels: new-entry
---

## Claim name

<!-- e.g. "Llama 3 Paper — HumanEval pass@1" -->

## Canonical public source

<!-- A primary source: paper, official model card, or vendor release notes.
     Third-party summaries (blog posts about the paper) do not qualify. -->

URL:
Date of source:

## Proposed bits (9 fields, 0 or 1)

| # | Criterion | Bit | Evidence (quote + offset) |
|---|---|---|---|
| 1 | metric_named | | |
| 2 | value_given | | |
| 3 | dataset_named | | |
| 4 | dataset_hash | | |
| 5 | model_version_pinned | | |
| 6 | threshold_direction | | |
| 7 | sample_size | | |
| 8 | seed_published | | |
| 9 | pre_registered | | |

## Note (≤ 80 words)

<!-- Describe the *structural* gap, not the publisher. Neutral language only.
     Bad:  "Vendor X is hiding their seed."
     Good: "Seed is not part of the published format for this release type."
-->

## Confirmation

- [ ] I have linked the canonical primary source above
- [ ] I have quoted text or pointed to specific document offsets
- [ ] My note describes the format, not the publisher
- [ ] I have read CONTRIBUTING.md
