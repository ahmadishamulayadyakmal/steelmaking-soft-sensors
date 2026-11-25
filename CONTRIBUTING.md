# Contributing

Contributions are welcome through issues and pull requests. Keep code,
documentation and commit messages in **English**.

## Pull requests

1. Branch from `main` with a short descriptive name.
2. Keep the test suite green locally and in GitHub Actions.
3. Document the change in `README.md` and `CHANGELOG.md` when relevant.
4. Describe the evidence behind any new number: dataset, licence, checksum,
   DOI, analytical benchmark and uncertainty estimate.

## Evidence standard

- Use open datasets and published literature only. No plant or proprietary
  data belongs in this repository.
- Every reported number needs provenance: dataset checksum, DOI, or an
  analytical benchmark with an error estimate.
- Numbers quoted from papers are external literature and must never be
  presented as independently reproduced results.
- Never commit API keys, raw downloaded datasets or publisher PDFs.

## Reporting templates

- `docs/model_card.md` — intended use, data, metrics and limitations.
- `docs/vv_template.md` — verification and validation report structure.
