# Documentation index

This repository is one of the 12 case repositories of the computational
metallurgy portfolio. Case specification and claim boundaries are in the
root `README.md`; the master plan, journal list and repository map live in a
**separate planning repository** and are linked from the root README.

## Local guide

- `README.md` — case specification with the six mandatory sections
- `CONTRIBUTING.md` — sprint contract, evidence rules and tag policy
- `sprints/wNN.md` — sprint note template; copy for each `wNN`
- `vv_template.md` — verification & validation report template
- `model_card.md` — model card template for any trained model
- `.github/` — sprint issue template, PR template and starter CI

## Before the first sprint

1. Copy `sprints/wNN.md` to `sprints/wNN.md` with the real week number.
2. Read the reference IDs listed in `README.md` and record access status in
   `JOURNALS.md` in the planning repository.
3. Add every dataset to `data/SOURCES.md` (create it if this repository has a
   `data/` folder).
4. Keep the six README sections intact; tag `cNN` only when the case gate is
   met.

E01 uses a full Python + Fortran CI matrix; the other repositories start with
the generic hygiene + Python-test workflow in `.github/workflows/ci.yml`.
