# PRML Integrity Index

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20177839.svg)](https://doi.org/10.5281/zenodo.20177839)

> A public, reproducible scorecard of how well 25+ well-known ML evaluation claims meet the 9 falsifiability criteria PRML considers minimum hygiene.

🌐 **Live page:** [falsify.dev/integrity](https://falsify.dev/integrity)
📖 **Spec:** [spec.falsify.dev/v0.1](https://spec.falsify.dev/v0.1)
📜 **License:** CC0 1.0 — public domain dedication for data and tooling

---

## What this is

A snapshot dated 2026-Q2 that scores well-known evaluation claims (proprietary and open) against the eight-field PRML manifest format plus one extra criterion (pre-registration timestamp).

**This is heuristic, not authoritative.** The score reflects the canonical *public* source of each claim — what the publisher chose to record. Two claims with the same accuracy can score very differently here. That's the point: the score reflects format hygiene, not model quality.

## What this is *not*

- Not a moral ranking
- Not affiliated with, endorsed by, or written in cooperation with any of the listed publishers
- Not a tool to embarrass anyone — a low score reflects a format gap, not a conduct gap
- PRML §8.1 explicitly: a high score means a claim is *checkable*, not that it is *true*

## The nine criteria

1. **Metric named** — accuracy, refusal-rate, F1, etc.
2. **Numeric value** — a scalar, not "state of the art"
3. **Dataset named** — HumanEval, GPQA, MMLU, etc.
4. **Dataset hash / version pin** — a specific revision or content hash
5. **Model version pinned** — a build, date, or revision (not "GPT-4")
6. **Threshold direction stated** — `>= 0.95`, not "around 95%"
7. **Sample size given** — N for the eval run
8. **Seed published** — RNG state when applicable
9. **Pre-registration date** — timestamp showing the threshold was set before the run

## Disagree with a score?

**Open an issue.** Use the [Re-score request](.github/ISSUE_TEMPLATE/rescore.md) template:

- Link to the canonical public source (paper, model card, blog post)
- Name the field you think we missed
- Quote the relevant text or screenshot

We re-score on receipt of evidence. Re-scoring is cheap; arguing about scores is not the point.

## Add a new claim

Use the [New entry](.github/ISSUE_TEMPLATE/add-entry.md) template. Submissions must:

1. Cite a **public** primary source (academic paper, official model card, vendor release notes — not third-party summaries)
2. Be reproducible: anyone reading the source must be able to verify each of the 9 bits
3. Use neutral language in the `note` field — describe the structural gap, never the publisher

## Repository structure

```
data/
  entries.json       # canonical scored entries — single source of truth
  schema.json        # JSON schema for entries.json
.github/
  ISSUE_TEMPLATE/
    rescore.md       # template for re-score requests
    add-entry.md     # template for new entries
README.md            # this file
LICENSE              # CC0 1.0 — see file
CONTRIBUTING.md      # how to propose changes
```

The page at [falsify.dev/integrity](https://falsify.dev/integrity) is rendered from `data/entries.json` (currently inlined in the page; the repo is the auditable source).


## Audit & compliance crosswalks

Subcategory-by-subcategory maps from major AI governance frameworks to PRML fields (FULL / PARTIAL / NONE tagged):

- [EU AI Act Article 12](https://spec.falsify.dev/eu-ai-act/article-12/) — code-level pattern for the 2 August 2026 high-risk deadline
- [NIST AI RMF 1.0](https://spec.falsify.dev/nist-ai-rmf/) — GOVERN / MAP / MEASURE / MANAGE subcategory map
- [ISO/IEC 42001:2023](https://spec.falsify.dev/iso-42001/) — AI Management System clause-by-clause evidence map

## Versioning

The Index is versioned by quarter. A re-scored entry produces a delta entry in `data/changelog.md` so historical versions are reproducible.

- `2026-Q2` — initial release (this version)
- `2026-Q3` — planned: 50 entries, including more open-weight claims and AISI/METR-style audited evaluations

## License

- Everything in this repository (data, README, any tooling): **CC0 1.0** — public domain dedication. Mirror, fork, dispute, re-derive without attribution required.

## Authors

Cüneyt Öztürk, co-founder, Studio 11 Turkey Ltd. Şti.
Contact: hello@studio-11.co · [falsify.dev](https://falsify.dev)

The Index was produced as part of the PRML v0.1 launch (2026-05) and is maintained as a community resource. Submitting a re-score is not a hostile act; it is the intended workflow.


---

## Status

- v0.1 stable. v0.2 RFC open through 2026-05-22 — [spec.falsify.dev/v0.2-rfc](https://spec.falsify.dev/v0.2-rfc).
- The PRML JSON Schema is in the [SchemaStore catalog](https://www.schemastore.org/json/) (merged 2026-05-11), so `*.prml.yaml` files autocomplete in VS Code, JetBrains, Helix, Zed, and Cursor out of the box.

## Contributing

See [`CONTRIBUTING.md`](./CONTRIBUTING.md) and the [`good first issue`](https://github.com/studio-11-co/falsify-integrity-index/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22) label for scoped work.

**Cite the spec:** Öztürk, C. (2026). *PRML v0.1*. Zenodo. [https://doi.org/10.5281/zenodo.20177839](https://doi.org/10.5281/zenodo.20177839)
