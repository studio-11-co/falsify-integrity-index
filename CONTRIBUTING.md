# Contributing to the PRML Integrity Index

The Index is a community-maintained scorecard. Contributions are welcome and follow a narrow set of rules.

## What we accept

1. **Re-score requests** with evidence from a canonical public source
2. **New entries** with evidence from a canonical public source
3. **Schema/tooling improvements** that make the data more auditable
4. **Bug fixes** in the rendered page (`falsify.dev/integrity` is in a separate repo)

## What we don't accept

- Re-scores based on argument alone, with no quotable evidence
- Entries citing third-party summaries instead of primary sources
- Notes that name or shame a publisher
- Entries about a model whose canonical evaluation source is not yet public
- Submissions designed to embarrass a specific company

## How to submit

### Re-score

1. Open a [Re-score request](.github/ISSUE_TEMPLATE/rescore.md) issue
2. Wait for a maintainer reply (target: 5 business days)
3. Maintainer either re-scores or asks for additional evidence
4. Re-scored entries are reflected in `data/entries.json` with a delta in `data/changelog.md`

### New entry

1. Open an [Add new entry](.github/ISSUE_TEMPLATE/add-entry.md) issue
2. After triage, submit a PR adding the entry to `data/entries.json`
3. PR must validate against `data/schema.json`
4. PR must include a one-line addition to `data/changelog.md`

## Voice rules (mandatory)

The Index works because it is structural, not personal. To preserve that:

- Notes describe the **format**, not the publisher
- Use phrases like "structural gap," "format hygiene," "publishing convention"
- Do not use "hiding," "lying," "scandal," "exposed"
- A low score reflects a format the publisher chose; not a moral failing

If a contribution violates voice rules, a maintainer will rewrite the note rather than reject the entry. The factual content is more valuable than the prose, so we keep the data and fix the voice.

## Maintainer review

Maintainers re-score when:

- Evidence is quoted from a primary source
- The claim about the field is verifiable in under 5 minutes
- The proposed change is consistent with the criteria definitions

Maintainers decline to re-score when:

- The evidence is interpretive (e.g. "the publisher implied X")
- The source is not accessible to the public
- The claim depends on inferring intent

## License

By contributing, you agree that:

- Data contributions (entries, notes) are released under **CC0 1.0**
- Tooling contributions (scripts, schemas) are released under **MIT**
- You have read and accepted the voice rules
- Your contribution is your own work or properly cited

## Maintainers

Cüneyt Öztürk · hello@falsify.dev
