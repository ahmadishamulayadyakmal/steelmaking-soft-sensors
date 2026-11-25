# C05 · Steelmaking soft sensors and steel fatigue — W18–W21

> **Real industrial case dossier.** Copied from the authoritative case card in
> `CASES.md` §4 so this repository stays self-contained after it is pushed to
> GitHub. Planning links: [`CASES.md`](https://github.com/ahmadishamulayadyakmal/metallurgy-project/blob/main/CASES.md) ·
> [`JOURNALS.md`](https://github.com/ahmadishamulayadyakmal/metallurgy-project/blob/main/JOURNALS.md) ·
> [`WEEKLY_PLAN.md`](https://github.com/ahmadishamulayadyakmal/metallurgy-project/blob/main/WEEKLY_PLAN.md).
> **Evidence level: A + B** · No plant data is held in this repository.

**Repository:** `e05-calphad-mechanical-properties` · **Evidence: A + B** ·
**References:** R09, R10, R12, R13, Y2R01, Y2R02, Y2R03, Y2R12, D05.

**Industrial problem.** Three real control problems: (i) BOF endpoint
carbon/phosphorus/temperature (Tata Steel, 28,000 heats, Y2R01); (ii) blast-
furnace hot-metal silicon with delayed sampling (Gary Works, Y2R02); (iii) EAF
slag-foaming height, unmeasurable online (Y2R03). Plus fatigue strength of
NIMS steels (Y2R12), where destructive testing is slow and expensive.

**Why it happens.** Delayed or missing online measurements; strong process
nonlinearity; plant data are confidential.

**Data (open + journal).** NIMS MatNavi / Agrawal supplementary data (A, D05),
MatBench steels (A), and **journal-documented** plant results (B) used only as
external literature. Open or documented synthetic surrogates reproduce the
*methods* for the three B control problems.

**Tool chain.** `metalkit` schema → `pycalphad` thermodynamic features (R13) →
hybrid heat/mass-balance + ANN (Y2R01) → leakage-safe time split + XGBoost
(Y2R02) → LSTM + sensitivity pruning (Y2R03) → SHAP (R12) → conformal intervals
→ model card.

**What each reference validates.**
- R09, R10, Y2R12 — fatigue datasets, RF/XGBoost comparators, error-modality
  warning.
- R12 — thermodynamic features + interpretability.
- R13 — `pycalphad` equilibrium features.
- Y2R01 / Y2R02 / Y2R03 — the three industrial control problems and their
  **external, non-reproduced** plant numbers.
- D05 — NIMS / Agrawal dataset provenance.

**Deliverables.** `cases/bof_endpoint/`, `cases/bf_silicon/`,
`cases/eaf_foaming/`, `cases/nims_fatigue/`; calibration plots; SHAP-vs-
metallurgy check; conformal coverage table; four model cards.

**Validation.** Conformal empirical coverage reported; no random split across
time; B-level statement in every B case; 3.7% / 9.77% / 91% / 0.905 / R² > 0.97
appear **only** as cited external literature.

**Acceptance.** Every B case contains the exact §1 disclaimer sentence; A-level
fatigue case reports error modality, not only R².

## Claim boundary

See [`evidence.md`](evidence.md) for the evidence level and the exact wording
that must be used when quoting literature numbers. All datasets and references
are listed in [`sources.md`](sources.md); the four-week execution plan is in
[`week_plan.md`](week_plan.md).
