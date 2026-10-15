# Lesson 07 — Beyond Averages

## Behavioural Profiling with Unsupervised Machine Learning

One population does not necessarily mean one set of needs. Explore synthetic global-health and e-commerce data, compare K-means and Ward hierarchical clustering, and interpret population profiles responsibly.

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/amobionovo/EvidenceLab/blob/main/lessons/07-behavioural-profiling/EvidenceLab_07_Behavioural_Profiling_Beginner_Guided.ipynb)

[Read or download the beginner-guided notebook](EvidenceLab_07_Behavioural_Profiling_Beginner_Guided.ipynb) · [Download journal-style outputs](EvidenceLab_07_Journal_Outputs.zip) · [Verification record](QA.json)

Select **Runtime → Run all**, then read from top to bottom. Both datasets are generated automatically; no upload or API key is needed.

The final beginner-guided edition adds step-by-step explanations and learner questions. All 27 tables have horizontal scrollbars for viewing every column. The [journal edition](EvidenceLab_07_Behavioural_Profiling_Journal.ipynb) remains available.

### Figures and tables

The notebook produces 16 numbered figure sets and 27 numbered tables. Figures export as SVG, PDF and 300-dpi PNG. Tables export full-precision CSVs, styled HTML, and print-ready PNG/SVG/PDF pages. Captions state data provenance, units, denominators and interpretive limits. Dense scatter points are rasterised within vector containers to keep files manageable; vector labels remain editable.

White backgrounds, restrained teal/orange accents, marker shapes, consistent typography and aligned comparison axes support print and notebook use. Check the chosen journal's exact page dimensions and submission requirements when adapting these general journal-style exports.

![Observed health profiles in original units](evidencelab07_outputs/figures/09_health_profile_medians.png)

*Printed cells show observed medians in original units. Colour shows standardised median contrasts, not uncertainty or intervention effects. Cluster labels are method-specific.*

### Scientific interpretation

The primary models use full transformed feature matrices; two-dimensional PCA is a projection. PCA-reduced modelling is compared separately. The highest-silhouette starting candidate is K = 2 for each synthetic dataset, despite four hidden generating patterns. A stable partition need not recover the generating patterns or establish service needs.

Categorical profiles include a Missing level and use all records within each cluster as their denominator. Numeric means and medians use observed values, with nonmissing sample sizes reported. The supplied notebook's data generators, feature preparation, primary model settings and original diagnostic results are preserved; both algorithms now receive symmetric profile tables and figures.

The published Nigerian HIV example reports 11,589 records, 313 supported clinics and six profiles. It is contextual evidence, separate from these synthetic data. [Read the original study](https://www.longdom.org/open-access/aggregating-loss-to-followup-behavior-in-people-living-with-hiv-on-art-a-cluster-analysis-using-unsupervised-machine-learning-algo-1102545.html).

### Infographic

![Lesson 07 infographic](assets/behavioural_profiling_infographic.png)

### Explainer preview

![Lesson 07 video preview — Beyond Averages](assets/behavioural_profiling_thumbnail.png)

[Download the final narrated explainer — 106.8 seconds, 1080p](video/EvidenceLab_07_FINAL_106_8s.mp4) · [Download subtitles](video/EvidenceLab_07_FINAL_106_8s.srt) · [High-resolution thumbnail](assets/behavioural_profiling_thumbnail_master.png)

The final video retains Helena’s narration and includes animated clustering demonstrations, sequential workflow charts and the Nigerian HIV example. YouTube link pending; it will be added when supplied by the owner.

Created by **Dr. Amobi Andrew Onovo, PhD, MPH**  
Epidemiology | Data Science | AI for Global Health  
**EvidenceLab | See it. Understand it. Run it.**
