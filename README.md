# Steelmaking soft sensors and steel fatigue (C05)

## Industrial problem

Real control problems: BOF endpoint carbon/phosphorus/temperature (Tata Steel, 28,000 heats); blast-furnace hot-metal silicon with delayed sampling (Gary Works); EAF slag-foaming height unmeasurable online. Plus fatigue strength of NIMS steels, where destructive testing is slow.

**Why it happens.** Delayed or missing online measurements, strong process nonlinearity, and confidential plant data.

## Data (no plant data)

Mixed: NIMS MatNavi / Agrawal supplementary data (D05), MatBench steels, and journal-documented plant results used only as external literature. Open or documented synthetic surrogates reproduce the methods where plant data cannot be released. No plant data is held.

> Only open datasets and published literature are used. No plant or proprietary data are held here; plant numbers quoted from papers are external literature, not independently reproduced results.

## Tool chain

`metalkit` schemas, `pycalphad` thermodynamic features, hybrid heat/mass-balance + ANN, leakage-safe time split, XGBoost, LSTM, SHAP, conformal prediction, calibration plots, model cards.

## Journal references

- **R09** ([DOI](https://doi.org/10.1007/s11431-020-1599-5)) — 360 NIMS steels, RF comparator, key feature families.
- **R10** ([DOI](https://doi.org/10.1007/s12541-019-00048-6)) — XGBoost fatigue comparator and external R2.
- **R12** ([DOI](https://doi.org/10.1016/j.mtcomm.2025.112674)) — thermodynamic features + interpretability.
- **R13** ([DOI](https://doi.org/10.5334/jors.140)) — `pycalphad` equilibrium features.
- **R14** — CALPHAD Gibbs/sublattice model foundations (compound: 2 papers).
- **R15** — CALPHAD book reference.
- **Y2R01** ([DOI](https://doi.org/10.3390/met12050801)) — BOF endpoint problem + external, non-reproduced plant numbers.
- **Y2R02** ([DOI](https://doi.org/10.3390/ma18030632)) — blast-furnace silicon problem + external 91% figure.
- **Y2R03** ([DOI](https://doi.org/10.1016/j.jmrt.2021.02.085)) — EAF slag foaming + external RMSE/R2 figures.
- **Y2R12** ([DOI](https://doi.org/10.1186/2193-9772-3-8)) — NIMS fatigue dataset, error-modality warning.
- **D05** ([DOI](https://doi.org/10.1186/2193-9772-3-8)) — NIMS / Agrawal dataset provenance.

## Deliverables

`cases/bof_endpoint/`, `cases/bf_silicon/`, `cases/eaf_foaming/`, `cases/nims_fatigue/`; calibration plots; SHAP-vs-metallurgy check; conformal coverage table; four model cards.

## Validation & claims

Conformal empirical coverage reported; no random split across time; external plant numbers are labelled as such wherever they appear; 3.7% / 9.77% / 91% / 0.905 / R2 > 0.97 appear ONLY as cited external literature.

## Limitations

Plant numbers quoted from cited papers are external literature and were not independently reproduced; results are comparable in method only, not in plant validation. No safety claim.

## Repository layout

- `README.md` — case summary, data policy, method, results and limitations.
- `CONTRIBUTING.md` — how to propose changes.
- `docs/index.md` — documentation map.
- `docs/model_card.md` and `docs/vv_template.md` — reporting templates.
- `.github/workflows/ci.yml` — automated checks.

Only open data and published literature are used. No plant or proprietary data
are included. All artefacts are written in English.
