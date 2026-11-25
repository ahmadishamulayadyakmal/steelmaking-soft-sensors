# Contributing

Every sprint in this repository follows the same contract. Keep all artefacts in
**English**. Codes (`W01`–`W104`, `C01`–`C12`, `Rxx`) stay verbatim.

## Branch and pull request flow

1. Branch from `main` as `wNN/<short-topic>`.
2. Open one PR per sprint; the PR title is the sprint title.
3. Keep tests green locally and in GitHub Actions.
4. Add one new artefact and one README paragraph; update `CHANGELOG.md`.
5. Write the sprint note `docs/sprints/wNN.md`.
6. After merge, tag `wNN` on `main` and push tags.
7. At case completion, tag `cNN` only after all six README sections are present.

## Weekly Definition of Done

1 merged PR · green tests · 1 new artefact · 1 README paragraph ·
1 sprint note · tag `wNN`. On Wednesday, cut 30% of the scope if needed;
carry-over is limited to one week. Review weeks are buffers.

## Evidence rules

- **No plant data.** Use open datasets and peer-reviewed journals only.
- Every number needs provenance: dataset + checksum, journal DOI, or an
  analytical benchmark with an error estimate.
- Level B plant numbers quoted from a paper are **external literature**.
  Carry the exact disclaimer from `CASES.md` §1 and never claim plant
  validation.
- Record every dataset in `data/SOURCES.md` in the owning repository.
- Never commit API keys, raw downloaded datasets or publisher PDFs.

## Templates

- Sprint note: `docs/sprints/wNN.md`
- V&V report: `docs/vv_template.md`
- Model card: `docs/model_card.md`

Planning documents (`CASES.md`, `JOURNALS.md`, `REPOSITORIES.md`,
`WEEKLY_PLAN.md`) live in the separate planning repository linked from
`README.md`.
