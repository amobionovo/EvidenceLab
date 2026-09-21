# Scientific methods and claim ledger

The original final supplied infographic remains unchanged. A separate distribution copy corrects only the notebook QR, as subsequently requested; no artwork or scientific content was redesigned. SHA-256: `a4373873994e94fa2993cb4a63fcb12139f70acd98fd0d256d48ab18b4daa95b`. Its poster values (0.42, 0.28, 0.24) are not calibration targets. Every new chart and numerical claim comes from the notebook's outputs.

## Definitions and estimands

- First-event competing risk: a competing event precludes the event of interest under the endpoint definition. Death before first relapse is an unambiguous example.
- Censoring: the event time is incompletely observed. Independent censoring, possibly conditional on modeled covariates, is an identification assumption; no diagnostic establishes it from observed data alone.
- Absolute event probability: CIF_k(t) = P(T ≤ t, J=k). Aalen–Johansen combines overall event-free survival with cause-specific event increments.
- Cause-specific hazard: instantaneous type-k event rate conditional on still being event-free. Coding other causes as censored in a Cox implementation removes those subjects from this risk set; independent hypothetical latent event times are not required to define the observed cause-specific hazard.
- Fine–Gray: covariates model the subdistribution hazard associated with a CIF. Modified risk sets are mathematical constructs. An sHR is not a probability or risk ratio. Proportional subdistribution hazards and appropriate censoring treatment require assessment.

## Implementation decision

Execute lifelines 0.30.3 KM, Aalen–Johansen and cause-specific Cox. Keep Fine–Gray conceptual. This release does not assert that no Python Fine–Gray package exists; it selects a documented, independently checked Python teaching stack that has no documented Fine–Gray fitter. The CRAN cmprsk implementation is a further-study reference, not a hidden dependency or claimed fitted result.

Colab setup installs only lifelines 0.30.3, retaining Colab's preloaded numerical stack. A first test that replaced base packages failed due to mixed loaded NumPy versions. That failed run is not counted as a successful Colab validation. Package versions are printed on every successful run; local pinned baseline is recorded separately.

## Simulation

2,500 entirely artificial records; seed 201703; maximum 60 months. Covariates: age, simplified binary sex, randomized exposure, measured baseline score. Exponential latent clocks have covariate-dependent rates; censoring is generated independently. Conditional proportional primary hazards hold by construction. These synthetic exposure coefficients are not real clinical effects.

Scenario analysis reuses seed, covariates, primary clocks and censoring draws, varying only the competing hazard multiplier (.25, 1, 2.5). The estimand remains first relapse before death. It is a model-based experiment, not a causal intervention estimate.

## Independent tests

See [independent checks](independent_science_checks.json), [clean Colab validation](colab_validation.json), and [QR-only change validation](qr_validation.json):
- lifelines CIF vs scikit-survival competing-risk estimator;
- lifelines KM vs scikit-survival KM;
- lifelines Cox vs statsmodels PHReg with Efron ties;
- independently written grouped risk-set recursion;
- hand-calculated tied-event case and no-censoring proportions;
- large independent simulation against the two-exponential closed-form CIF;
- probability conservation, bounds, monotonicity and paired scenario ordering;
- original and copied infographic hash unchanged.

## Historical claims

MOPEB0307, IAS 2017, Paris, 23–26 July 2017, appears on printed page 79. Title: “Demographic correlates of survival in adult HIV-infected patients initiating first-line antiretroviral therapy in Nigeria: a 7-year prospective cohort study.” Author list begins A. Onovo. The abstract explicitly accounts for LTFU with competing-risk regression. The supervisor conversation and personal learning story are the owner's supplied account; they are not independently documented in the abstract. No claim that the model addition caused acceptance is made.

LTFU does not prevent death biologically. It may be informative missing outcome information for mortality; for a first recorded program outcome it may be defined as another endpoint. Explain tracing/linkage, sensitivity analysis and multi-state alternatives; do not universalize the historical coding choice.

## Primary sources checked

- [IAS abstract book](https://www.ias2017.org/Portals/1/Files/IAS2017_LO.compressed4c6a.pdf?fileticket=m3LSDs1z4QY%3d&tabid=577&portalid=1).
- [lifelines Aalen–Johansen](https://lifelines.readthedocs.io/en/latest/fitters/univariate/AalenJohansenFitter.html).
- [lifelines regression](https://lifelines.readthedocs.io/en/latest/Survival%20Regression.html).
- [lifelines PH diagnostic](https://lifelines.readthedocs.io/en/latest/jupyter_notebooks/Proportional%20hazard%20assumption.html).
- [scikit-survival CIF](https://scikit-survival.readthedocs.io/en/stable/api/generated/sksurv.nonparametric.cumulative_incidence_competing_risks.html).
- [Fine & Gray 1999](https://doi.org/10.1080/01621459.1999.10474144).
- [cmprsk manual](https://cran.r-project.org/web/packages/cmprsk/cmprsk.pdf).

Core message: **Define the event → identify what can happen first → choose the estimand → then choose the model. Different models answer different questions.**

## Accessibility revision — 21 September 2026

The existing notebook now has 51 cells, including 24 code cells. New output cells translate the fitted KM/CIF and Cox results and the three scenario probabilities into plain language. Simulation and direct Aalen–Johansen helper functions are unchanged. Local records, full-precision results, Cox and diagnostic tables, scenario results and chart coordinates exactly match the previously validated release. A fresh Google Colab Run all completed all 24 code cells; its generated interpretations and numerical results were checked against the reference. See [revision validation](accessibility_v2_validation.json). Fine–Gray remains conceptual.
