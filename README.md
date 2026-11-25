# Steelmaking soft sensors and steel fatigue (C05)

> Workspace folder: `e05-calphad-mechanical-properties` · Suggested GitHub repository: `steelmaking-soft-sensors`
> Epic: E05 · Weeks: W18–W21 · Evidence level: **A + B**
> Master specification: [`CASES.md`](https://github.com/ahmadishamulayadyakmal/metallurgy-project/blob/main/CASES.md) §4 · Download the papers: [`JOURNALS.md`](https://github.com/ahmadishamulayadyakmal/metallurgy-project/blob/main/JOURNALS.md)

## Industrial problem

Real control problems: BOF endpoint carbon/phosphorus/temperature (Tata Steel, 28,000 heats); blast-furnace hot-metal silicon with delayed sampling (Gary Works); EAF slag-foaming height unmeasurable online. Plus fatigue strength of NIMS steels, where destructive testing is slow.

**Why it happens.** Delayed or missing online measurements, strong process nonlinearity, and confidential plant data.

## Data (no plant data)

Mixed: NIMS MatNavi / Agrawal supplementary data (A, D05), MatBench steels (A), and journal-documented plant results (B) used ONLY as external literature. Open or documented synthetic surrogates reproduce the methods for B cases. No plant data is held.

> The author cannot supply factory data. This project uses **only open datasets and
> credible peer-reviewed journals**. If this is a B-level case, the case report
> must contain the exact disclaimer from `CASES.md` §1 and must **never** claim
> plant validation.

## Tool chain

`metalkit` schemas, `pycalphad` thermodynamic features, hybrid heat/mass-balance + ANN, leakage-safe time split, XGBoost, LSTM, SHAP, conformal prediction, calibration plots, model cards.

## Journal references

- **R09** — 360 NIMS steels, RF comparator, key feature families.
- **R10** — XGBoost fatigue comparator and external R2.
- **R12** — thermodynamic features + interpretability.
- **R13** — `pycalphad` equilibrium features.
- **R14** — CALPHAD Gibbs/sublattice model foundations (compound: 2 papers).
- **R15** — CALPHAD book reference.
- **Y2R01** — BOF endpoint problem + external, non-reproduced plant numbers.
- **Y2R02** — blast-furnace silicon problem + external 91% figure.
- **Y2R03** — EAF slag foaming + external RMSE/R2 figures.
- **Y2R12** — NIMS fatigue dataset, error-modality warning.
- **D05** — NIMS / Agrawal dataset provenance.

Each reference above is listed with its DOI or stable URL, access status and
manual download route in [`JOURNALS.md`](https://github.com/ahmadishamulayadyakmal/metallurgy-project/blob/main/JOURNALS.md) §4, and in the shared
BibTeX library `papers/references.bib`. Do not cite a paper you have not been
able to obtain; if it is inaccessible, record that in `JOURNALS.md` §8.

## Deliverables

`cases/bof_endpoint/`, `cases/bf_silicon/`, `cases/eaf_foaming/`, `cases/nims_fatigue/`; calibration plots; SHAP-vs-metallurgy check; conformal coverage table; four model cards.

## Validation & claims

Conformal empirical coverage reported; no random split across time; B-level statement in every B case; 3.7% / 9.77% / 91% / 0.905 / R2 > 0.97 appear ONLY as cited external literature.

## Limitations

Every B case must state: plant numbers are from the cited paper and were NOT independently reproduced; our result is comparable in method only, not in plant validation. No safety claim.

## Definition of Done

1 merged PR · green tests · 1 new artefact · 1 README paragraph · 1 sprint note
`docs/sprints/wNN.md` · tag `wNN`. Before the case tag `c05` is created,
this README must contain all six sections: Industrial problem, Data (no plant
data), Tool chain, Journal references, Validation & claims, Limitations.

## Repository skeleton

Shared files: `CONTRIBUTING.md` (sprint contract), `.github/` (issue, PR and
CI templates), `docs/sprints/wNN.md`, `docs/vv_template.md` and
`docs/model_card.md`. `CASES.md`, `JOURNALS.md` and `REPOSITORIES.md` are in a
separate planning repository; their links above remain valid after this folder
is pushed as its own repository.

The real industrial case dossier is in `case/`: `README.md` (full case card),
`evidence.md`, `sources.md` and `week_plan.md`.

## Repository status and GitHub Desktop

This folder is already a Git repository on `main`, pushed to GitHub as
`steelmaking-soft-sensors` with an SSH `origin`. In GitHub Desktop, choose **Add local
repository** and select this folder; do not clone into the same path.

```bash
git status --short --branch
git pull --rebase origin main
git push origin main
```

Weekly work follows `CONTRIBUTING.md`: one PR, green tests, one artefact, one
README paragraph, `docs/sprints/wNN.md`, tag `wNN`. Tag `c05` only after
all six README sections are complete.


## Language

All artefacts in this repository are written in **English**.
