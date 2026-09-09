# EvidenceLab #01: 95% Confidence Interval vs 95% Credible Interval

**Same data. Different questions. Different meaning.**

[Back to EvidenceLab](../../README.md) · [View the notebook](confidence_vs_credible_intervals.ipynb)

## See it

![EvidenceLab infographic comparing frequentist confidence intervals and Bayesian credible intervals](assets/confidence_vs_credible_interval_infographic.png)


## Learning objectives

- Define a treatment effect and the direction of benefit.
- Calculate and interpret a 95% CI and recognize its common misinterpretation.
- Explain prior, likelihood, posterior, and a 95% credible interval.
- Distinguish repeated-sampling coverage from posterior probability.
- Observe coverage over 1,000 simulated studies.
- Explore prior sensitivity and the effect of sample size on uncertainty.
- Interpret the posterior probability of any benefit and of a specified benefit size.
- Explain why statistical evidence alone does not determine a public health decision.

## The simulated hypertension example

**All data are simulated for educational purposes. No observations represent real patients or a real clinical trial.**

The notebook generates independent normal outcomes for 45 participants in each group. The outcome is change in systolic blood pressure from baseline, measured in mmHg. The control population mean change is 0 mmHg, the treatment population mean change is −3 mmHg, and the population standard deviation is 10 mmHg in both groups.

**Treatment effect = average BP change in treatment group − average BP change in control group.** Negative values favor treatment because they represent a larger reduction in systolic blood pressure. The true effect is known in this simulation; in real research it is unknown.

## Understand it

| Term | Meaning in this lesson |
| --- | --- |
| Treatment effect | The difference between treatment and control mean SBP changes. |
| Confidence interval (CI) | An interval from a procedure that covers the fixed true effect in approximately 95% of repeated studies under the sampling and model assumptions. This notebook uses Welch's t interval. |
| Prior | A distribution expressing uncertainty about the effect before incorporating this study; the main example uses Normal(0, 10²), with standard deviation 10 mmHg. |
| Likelihood | How the observed estimate varies with the unknown effect under the model. Here, the estimate is approximated as normal with standard error estimated from the data. |
| Posterior | The updated distribution for the effect after combining the prior and likelihood. |
| Credible interval | An interval containing 95% of posterior probability, conditional on the model, prior, and observed data. Here it is an equal-tailed normal posterior interval. |

The Bayesian calculation treats the estimated standard error as fixed. It is an approximate normal–normal analysis, not a full Bayesian model of unknown group variances. The frequentist calculation uses a t critical value and Welch degrees of freedom. Their numerical differences reflect these modeling choices as well as the prior.

### Key numerical results

The following rounded values were reproduced by sequential execution of all 15 code cells. The run generated six figures and four tables without errors.

| Quantity | Default result |
| --- | --- |
| Participants per group | 45 |
| True simulated effect | −3.0 mmHg |
| Observed effect | −1.70 mmHg |
| Frequentist 95% CI | [−6.15, 2.74] mmHg; includes zero |
| Repeated studies | 1,000 |
| Observed CI coverage | 95.2% |
| Prior | Normal(0, 10²) |
| Posterior mean | −1.62 mmHg |
| 95% credible interval | [−5.90, 2.66] mmHg |
| P(effect < 0 ∣ model, prior, data) | 77.1% |

The CI's 95% refers to the long-run behavior of the procedure. It does **not** assign 95% probability to the fixed true effect being inside this particular observed CI. The credible interval's 95% refers to posterior probability under the specified Bayesian analysis.

The 77.1% probability concerns any negative effect, not necessarily a clinically meaningful benefit. The notebook also explores an illustrative −2 mmHg threshold. Real decisions need justified thresholds and consideration of harms, costs, feasibility, equity, and consequences.

## Run it

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/amobionovo/EvidenceLab/blob/main/lessons/01-confidence-vs-credible-interval/confidence_vs_credible_intervals.ipynb)

1. Click **Open in Colab**.
2. Select **Runtime > Run all**. No setup is required in the standard Python Colab runtime.
3. Follow the explanations, figures, and tables in order.
4. Change the parameters below and run all again.

The notebook uses NumPy, pandas, Matplotlib, and SciPy. All data are generated within it; no local input file, external dataset, API key, paid package, or patient data is required. Fixed seeds make the default example reproducible.

### Suggested experiments

1. Change `N_PER_GROUP` in the setup cell to explore sample size (use an integer of at least 2; try 20, 50, or 100).
2. Change `TRUE_EFFECT` in the setup cell; try 0 or −5 mmHg.
3. Change `PRIOR_SD` in the Bayesian inference cell to another positive value; try 3 or 20 mmHg.
4. Select **Runtime > Run all** after each change.
5. Observe how CI width changes.
6. Observe how posterior uncertainty changes.
7. Observe how posterior probability of benefit changes.

The prior-sensitivity section compares three separately specified priors. The sample-size section compares approximate expected widths for its own list of sample sizes; the study itself uses `N_PER_GROUP`. Changing sample size generates different simulated observations, so a single comparison may also reflect sampling variability.

## Key takeaway

**Same 95%. Different meaning.**

A confidence interval describes the long-run behavior of an interval-generating procedure.

A credible interval describes posterior uncertainty about a parameter, conditional on the model, prior, and observed data.

## Educational disclaimer

EvidenceLab is an educational resource. Examples and simulated datasets are intended for teaching statistical concepts and should not be interpreted as clinical recommendations or evidence about the effectiveness of any real treatment.

Created by **Dr. Amobi Andrew Onovo, PhD, MPH**  
Epidemiology | Data Science | AI for Global Health  
**EvidenceLab | See it. Understand it. Run it.**
