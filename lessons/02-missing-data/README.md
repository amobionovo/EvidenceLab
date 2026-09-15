# EvidenceLab #02: Missing Data in Real Life

**See the pattern. Before you fill the gap.**

[Back to EvidenceLab](../../README.md) · [View the notebook](missing_data.ipynb)

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/amobionovo/EvidenceLab/blob/main/lessons/02-missing-data/missing_data.ipynb)

## See it

![EvidenceLab missing-data reference: patterns, mechanisms, treatment, triangulation, sensitivity and leakage prevention](assets/missing_data_infographic.png)

## Two hands-on tracks

1. **Simulation laboratory:** create complete fictional data, deliberately hide values under MCAR, MAR and MNAR, and compare methods against known truth.
2. **Framingham investigation:** examine a cardiovascular-risk teaching dataset, investigate observed associations, compare methods, and stress-test conclusions. The natural missingness mechanism is unknown.

The Framingham teaching copy contains **388 missing glucose values among 4,240 records (9.15%)**. This percentage cannot establish MCAR, MAR or MNAR. The teaching CSV is not the full original Framingham Heart Study, and the notebook is not a clinical prediction tool.

## Understand it

Follow **MAP → QUESTION → MECHANISM → METHOD → STRESS-TEST → MODEL → INSIGHTS**.

- **MCAR:** missingness is independent of observed and unobserved values.
- **MAR:** conditional on observed information, missingness has no remaining dependence on the missing values.
- **MNAR:** dependence on unseen information remains after conditioning on observed information.
- Compare complete cases, simple baselines, regression, KNN, and PMM/MICE. Proper multiple imputation for inference retains uncertainty through repeated completions and Rubin pooling.
- The **Multi-Method Triangulation Check** compares plausibility, distributions, known-truth error where available, and downstream results. It is not an average of imputation methods.
- Sensitivity analysis asks whether conclusions survive another reasonable assumption about missing values.
- For prediction, split first, fit preprocessing within training or cross-validation folds, and apply the fitted transformation to test data.

**Agreement strengthens robustness. Disagreement is information.**

## Run it

1. Open the notebook in Colab.
2. Select **Runtime → Run all**. The setup cell installs missing packages.
3. Keep the defaults for a first run: simulation first, then the pinned, checksum-checked Framingham teaching mirror.
4. To supply your own compatible CSV, set `USE_UPLOAD = True` and use Colab's file picker.
5. Set `RUN_FRAMINGHAM = False` to explore simulation only.
6. Change a parameter, rerun, and compare the charts and tables.

Track 1 requires no uploaded dataset. Track 2 needs the teaching mirror or a compatible CSV. If the mirror is unavailable, the notebook reports this and Track 1 remains usable. Source attribution and the pinned mirror URL are documented inside the notebook. No raw CSV is redistributed in this lesson folder.

The notebook contains interactive charts and writes analysis outputs to `outputs/`. GitHub's static notebook view does not provide the full interactive experience; use Colab to execute it. Fixed seeds support reproducibility, but changed parameters or package versions can change results. The infographic's numerical charts are simulation benchmarks; they are not clinical findings.

## Video preview

![EvidenceLab Lesson 02 video thumbnail: Why is your data missing?](assets/missing_data_video_thumbnail.png)

**Video publication pending.** The approved explainer is complete; a YouTube link will be added after publication.

## Takeaway

Don't ask only: **“How much is missing?”**

Ask: **“Why is it missing, and does my conclusion still hold?”**

Created by **Dr. Amobi Andrew Onovo, PhD, MPH**
**EvidenceLab | See it. Understand it. Run it.**

Educational use only. See the repository [license](../../LICENSE).
