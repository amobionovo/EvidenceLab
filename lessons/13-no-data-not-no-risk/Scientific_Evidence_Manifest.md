# EvidenceLab #13 · Scientific evidence manifest

Primary source: Onovo AA, Atobatele A, Kalaiwo A, Obanubi C, James E, Gado P, Odezugo G, Ogundehin D, Magaji D, Russell M. *Using Supervised Machine Learning and Empirical Bayesian Kriging to reveal Correlates and Patterns of COVID-19 Disease outbreak in sub-Saharan Africa: Exploratory Data Analysis.* medRxiv preprint, posted 2 May 2020. doi:10.1101/2020.04.27.20082057. Not peer reviewed.

Verified on 19 November 2026 against the medRxiv full text (v1) and the Europe PMC record PPR157748.

## Claims shown or spoken

| # | Claim in the film | Where | Source text (paraphrased) | Status |
|---|---|---|---|---|
| 1 | 39 sub-Saharan African countries | VO scene 2, title card, "39 OF 48" | Methods: data for "39 of SSA's 48 countries that reported confirmed cases and deaths" | Verified |
| 2 | Study window 28 Feb to 26 Mar 2020 | Scene 2 timeline | Methods: "February 28, 2020 through March 26, 2020" | Verified |
| 3 | JHU surveillance data plus World Bank, WHO, UNICEF, UNAIDS indicators | VO and panels, scene 3 | Data Sources section and Acknowledgments | Verified. Panels are labelled as public data sources; no collaboration is shown |
| 4 | 19 candidate variables | Scenes 3 and 4 | "17 continuous and 2 categorical"; Research in Context: "nineteen explanatory variables" | Verified |
| 5 | Lasso-based methods; 7 statistically associated variables in the inferential analysis | VO and graphic, scene 4 | Cross-fit partialing-out Lasso: seven variables with p < 0.05 | Verified |
| 6 | The seven variables: time (days); HIV incidence ages 0–14, 10–19 and 15–24; PCV3 vaccine coverage (infants); malaria incidence; diarrhoea treatment under 5 | Scene 4 list | Results, Lasso for inferential statistics | Verified (see note A) |
| 7 | Associations are exploratory, not causal | VO and stamp, scene 4 | The preprint is titled exploratory data analysis | The film states this more cautiously than the preprint's own wording (note B) |
| 8 | EBK produced interpolated surfaces of reported distributions | Scenes 5 and 6 | Geospatial analysis: EBK in ArcGIS 10.8 Geostatistical Analyst; Figures 7 and 8 | Verified. The film's maps use teaching data, not the study's surfaces |
| 9 | Study points were country locations | Scene 2 chip "One location per country" | Discussion: "geocoordinate data ... represents locations of SSA countries not necessarily where COVID-19 disease was detected" | Verified (a limitation stated by the authors) |
| 10 | EBK accounts for uncertainty in the semivariogram through repeated simulation | VO and step 3, scene 5 | Method description (Krivoruchko; Esri Geostatistical Analyst documentation). Not a study result | Method fact |
| 11 | Ordinary EBK interpolates one measured variable; it does not ingest mobility, population or testing layers | Scene 7 chip "Integrated framework, not ordinary EBK" | Method fact. EBK Regression Prediction and other spatial regression models handle covariates | Method fact |
| 12 | Ebola preparedness in the DRC and neighbouring areas | Scene 7 | Conceptual example only. No Ebola data, case counts, probabilities or validation statistics are shown | Labelled conceptual on screen throughout the scene |

## Teaching data

Every map value in scenes 1, 5 and 6 comes from `tools/make_data.py` (seed 1313): a synthetic field sampled at 32 locations. The simplified EBK run fits an exponential semivariogram, simulates 100 refits and kriges with each model. The prediction is the mean across models. The standard error combines the mean kriging variance with the variance between models. The correlation between standard error and distance to the nearest observation is about 0.86. Every such frame carries the label ILLUSTRATIVE TEACHING DATA. The illustrative peaks were deliberately placed away from the study's reported patterns (South Africa and West Africa), so viewers cannot mistake them for study results. The Lasso coefficient path in scene 4 is illustrative and is labelled that way. Scene 7's layers are abstract patterns, not data.

## Notes for the record

- **A. Variable list inconsistency in the preprint.** The Measures section lists HIV incidence for ages 0–14 and 10–19 only. The selected variables also include "Incidence of HIV among individuals aged 15–24 years". The Discussion relabels the age groups (for example "adolescents aged 15–19"). The film shows the seven variables as named in the Results and does not name all 19 candidates. The missing 48 − 39 = 9 countries are not fully listed either: the Introduction names 6 exclusions. The film shows no country-level membership of the 39.
- **B. Causal language.** The preprint sometimes says variables "predict" or "raise the risk of" infection, reports doubling time and rate of change, and closes with a mass drug administration proposal. The film uses none of these findings. It presents the Lasso results only as exploratory statistical associations, as the owner's brief directs.
- No contemporary surveillance data are used, so no publication-date citation is needed in scene 7.
