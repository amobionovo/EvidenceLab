# EvidenceLab #05 notebook QA — controlled pedagogical upgrade

Date: 2 October 2026. Notebook: `EvidenceLab_05_Outliers_Anomalies_FINAL_v2.ipynb`.

**Final result: PASS for scientific preservation, reproducibility and desktop/Colab execution. Mobile portrait usability has a documented limitation; a fully responsive phone layout is not claimed.**

## Execution evidence

| Check | Result |
|---|---|
| Total cells | 31 |
| Markdown / code cells | 17 / 14 |
| Local fresh-kernel Run All | PASS twice; 2.94 s and 2.88 s |
| Hosted Google Colab | PASS after **Restart session and run all**; downloaded execution record checked |
| Hosted execution counts | 1–14, in notebook order |
| Cell errors / cell warnings | 0 / 0 in final local and hosted runs |
| Inline charts | All 7 PNG outputs present and decodable in hosted execution |
| Seed | 20261002 |
| Inputs / setup | No input files, uploads, API keys, package-install cells, widget actions or manual code edits needed |
| Reproducibility | All 24 exported files byte-identical across two fresh local kernels |

Local runtime: Python 3.12.14; NumPy 2.5.3; pandas 3.0.6; Matplotlib 3.11.2.

Hosted runtime: Python 3.13.15; NumPy 2.1.3; pandas 2.2.3; Matplotlib 3.10.0, standard Google Compute Engine Python backend. Hosted elapsed execution time was not measured independently; execution order and completion were verified from the downloaded notebook. Cross-platform floating-point coefficients agree within 1e-10 absolute / 1e-12 relative tolerance; cross-platform PNG byte identity is not claimed.

The local Windows kernel launcher emitted a Proactor/ZeroMQ selector fallback warning and a local TCP transport diagnostic. Neither was a notebook-cell or hosted Colab failure. An initial new-cell date-rounding warning was removed by rounding numeric columns only. No non-interactive Matplotlib warning appeared in final notebook outputs.

## Preservation and reproducibility

The complete original 25-cell notebook was reviewed before editing. The original notebook remains unchanged; SHA-256: `80de2db4a1ae451649089e756d1c0890d4d8c4cb2d43f946d4b7d297dec58177`.

Eleven of the twelve original code cells are byte-identical. The only changed original code cell is the export manifest: a deterministic list replaces a directory scan that could include stale files or include the manifest itself only on subsequent runs. A planted unrelated file stayed outside the manifest. No analytical calculation changed.

All **15 original CSV exports and six original PNG charts** are byte-identical to the original release in the same local environment. Original data generation, seed, treatment comparisons, baseline fit, sensitivity experiments, coefficients and summary results are preserved. Two new code cells add a boxplot anatomy view of existing values and an existing September 2025 monitoring-row illustration; neither draws random numbers or changes the model.

## Numerical consistency

- Small example: Q1 = 278.75; Q3 = 352.50; IQR = 73.75; fences = 168.125 and 463.125. July = 850 is flagged; observed whisker endpoints = 240 and 395, distinct from fences.
- The confirmed synthetic transcription error is corrected from 12,500 to 1,250; original recorded values remain available. The verified campaign value of 2,050 is retained.
- Raw mean = 1,580.361111; source-corrected mean = 1,267.861111; raw 1st/99th-percentile capped mean = 1,479.570833; corrected capped mean = 1,265.586111. Median = 1,176.5. These answer different questions; capping does not repair an error.
- September 2025: observed corrected value = 1,690; model expectation = 1,219.936917; residual = 470.063083; robust residual score = 20.237025. The approximate 1,700-versus-1,200 teaching example is explicitly linked to this row. It is not globally IQR-flagged but has a sustained time-aware alert.
- First sustained alert remains 2025-09-01, requiring three consecutive positive residual flags. The baseline uses the first 24 months with the campaign excluded and no future fitting.
- Threshold multipliers 2.5, 3.5 and 4.5 preserve the first sustained-alert date; prospective flags are 8, 6 and 6 respectively. This synthetic stability does not establish real-world calibration.

## Scientific review

PASS: sample quantiles and interpolation are explained; IQR flags prompt investigation; whiskers are observed values inside fences. Outliers, contextual/collective anomalies and confirmed errors remain distinct. Robust statistics and MAD receive intuition without changing formulas. Winsorization preserves rows but changes values and requires sensitivity analysis. Surveillance thresholds are heuristic, not calibrated prediction intervals. Synthetic source verification is labelled as fictional; no real timestamp or provenance was invented. Original values, correction reason and action remain auditable.

## Beginner and rendering review

PASS: the 12,500 opening offers four responses and explains investigation; the eight-step roadmap precedes analysis. Five-number summary, IQR steps, labeled boxplot anatomy, three-event comparison, outlier/anomaly table, robust-statistics intuition, treatment interpretations, surveillance explanation, decision aid and five final takeaways are present. Requested learner guidance labels are used. Reflection prompts never block execution.

Desktop Colab rendering was inspected at 1280×720. Headings, prose and opening choices render clearly. The added boxplot was visually reviewed for label/arrow clarity, and all seven hosted chart outputs decoded successfully. The original six local figures are unchanged.

**Mobile limitation:** at a simulated 390×844 viewport, Colab's editor pane extends beyond the visible width and requires horizontal scrolling. Text and headings render, but this does not pass a strict “no horizontal scrolling” portrait usability criterion. At 844×390 landscape width, reading is easier. This was browser viewport testing, not a physical phone test. Use desktop or landscape for the full code/tables. The notebook does not change Colab's application layout.

## Generated deliverables

- `EvidenceLab_05_Outliers_Anomalies_FINAL_v2.ipynb` — executed, self-contained v2; original retained beside it.
- `outputs_v2/` — 24 files: 16 CSVs, seven PNG figures and `analysis_manifest.json`.
- New outputs: `07_boxplot_anatomy.png` and `anomaly_manifest_v2_context.csv`.
- Running the notebook creates `outputs/` automatically; `outputs_v2/` is the delivery-folder name used to preserve the original release exports.
- `Notebook_V2_QA/` — local/hosted QA records, preservation audit, executed hosted notebook and layout screenshots.

**Release assessment:** scientifically and computationally ready; mobile portrait limitation disclosed. An unusual value is a question to investigate, not an instruction to delete.
