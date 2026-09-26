# EvidenceLab #04 notebook QA

- Status: PASS; two fresh-kernel executions, zero cell errors.
- Cells: 48 total; 29 markdown; 19 code.
- Runtime: 7.70s and 1.80s locally (Python 3.12.14, Windows).
- Packages: NumPy 2.5.3; pandas 3.0.6; matplotlib 3.11.2; nbformat 5.11.1; nbclient 0.11.0.
- Seed: 20260925. All 12 exported files are byte-identical across both runs.
- Four figures produced notebook image outputs: opening comparison, IFR posterior, surveillance experiment and final timing comparison. Opening, posterior and surveillance PNGs visually reviewed: legible labels and no clipping. Final SVG source and output dimensions checked.
- Python execution warnings: none. Local kernel launcher emitted TCP transport and shutdown notices; notebook cells produced no warnings or stderr.
- Notebook stderr: [].
- Original notebook SHA256, unchanged: `6742cf235d445e0d1efcf54a9b6fb058e2b4ccdbc0ef145157ba232fa71aa5d6`.

## Scientific checks
1,000 cases; 30 early deaths; 50 final deaths; early CFR 3%; completed CFR 5%; survey infections 10,000; IFR 0.5%.
One duplicate removed and one impossible diagnosis date quarantined. Conflicting IDs raise an error.
The day-42 survey is explicitly later than the day-21 snapshot. All simulated deaths are detected.
Posterior intervals are conditional on fixed assay/death assumptions. The published arithmetic is separate from the teaching model.
Surveillance experiment verifies CFR 5%, 2.5%, 1%, 0.5%, with IFR fixed at 0.5%.

## Beginner usability
No dataset download, input(), API key, absolute local path, pip installation or manual configuration in notebook cells.
Only NumPy, pandas, matplotlib and IPython are required in the standard Colab Python runtime.
Optional ipywidgets control has an ImportError fallback; complete static outputs run before it.
Original cleaning, survey, Bayesian, sensitivity, published-study, exercise and export content retained.
Local fresh-kernel execution is verified; hosted Google Colab execution is not claimed.

## Automatically generated outputs
- `ascertainment_scenarios.csv`
- `cleaning_audit.json`
- `comparison.svg`
- `ifr_uncertainty.png`
- `paper_arithmetic.json`
- `results.json`
- `sensitivity.csv`
- `surveillance_experiment.csv`
- `surveillance_experiment.png`
- `synthetic_cases_clean.csv`
- `synthetic_cases_raw.csv`
- `synthetic_survey.csv`
