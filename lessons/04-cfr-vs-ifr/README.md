# EvidenceLab #04: CFR vs IFR

## When the Denominator Changes the Story

**A 5% CFR does not mean 5% of everyone infected will die.**

[![Open Lesson 04 in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/amobionovo/EvidenceLab/blob/main/lessons/04-cfr-vs-ifr/EvidenceLab_04_CFR_vs_IFR_FINAL.ipynb)

[![EvidenceLab 04: 50 deaths, 1,000 detected cases and 10,000 estimated infections](assets/cfr_vs_ifr_thumbnail.png)](https://colab.research.google.com/github/amobionovo/EvidenceLab/blob/main/lessons/04-cfr-vs-ifr/EvidenceLab_04_CFR_vs_IFR_FINAL.ipynb)

*Synthetic completed-cohort example with complete death ascertainment. Person icons are illustrative;
the stated counts determine the percentages. CFR and IFR are proportions, commonly called fatality rates.*

## Run the lesson

1. Open the notebook using the Colab button above.
2. Select **Runtime → Run all** in the standard Python runtime.
3. Read from top to bottom: data, calculations, charts and exports are generated automatically.

No dataset upload, API key, file-path change or manual installation is required.
An optional surveillance slider complements a complete static table and chart.

## Follow the evidence

- Start with **CFR = 50 deaths ÷ 1,000 detected cases = 5.0%**.
- Compare **IFR = 50 deaths ÷ 10,000 estimated infections = 0.5%**.
- Clean a synthetic case register with an audit trail.
- Separate day-21 surveillance from completed follow-up.
- Estimate infections using survey evidence and assay correction.
- Quantify conditional Bayesian uncertainty and stress-test assumptions.
- Explore how improved detection changes CFR in a fixed infection cohort.
- Examine the published model-based analysis of 48 African countries.

IFR requires a defensible infection denominator, matched deaths and timing, and uncertainty.
CFR remains useful for detected-case outcomes. Neither measure automatically solves incomplete
follow-up or changing surveillance during outbreak onset.

## Published study

[Onovo et al. (2021), *Estimates of the COVID-19 Infection Fatality Rate for 48 African Countries:
A Model-Based Analysis*, BioMed](https://www.mdpi.com/2673-8430/1/1/5).

The notebook illustrates the reported aggregate arithmetic and explains the study assumptions.
Its synthetic survey analysis is a separate teaching example, not a replication of the published model.

## Lesson materials

- [Executed notebook](EvidenceLab_04_CFR_vs_IFR_FINAL.ipynb)
- [Notebook QA and reproducibility checks](EvidenceLab_04_NOTEBOOK_QA.md)
- [Thumbnail](assets/cfr_vs_ifr_thumbnail.png)
- [Companion infographic](assets/cfr_vs_ifr_infographic.png)

The video publication link is pending.

**Before interpreting a fatality percentage, ask who entered the denominator.**

Dr. Amobi Andrew Onovo · EvidenceLab | See it. Understand it. Run it.
