# econ3916-lab08-hypothesis-testing
Econ 3916 Lab 08 - Hypothesis Testing
# Hypothesis Testing: Is Job Training Worth It?

## Objective

I tested whether the LaLonde NSW job training program raised 1978 earnings, and how large and how reliable that effect is.

## Methodology

- Loaded the LaLonde NSW job training experiment: 445 people, 185 trainees and 260 controls.
- Ran a one-sample t-test and a two-sample Welch's t-test on 1978 earnings.
- Wrote Welch's t-statistic as a function, `welch_t()`, and checked it against scipy on the full sample and on five subgroups.
- Computed Cohen's d to judge the size of the effect, not only whether it is significant.
- Ran a power analysis to find the power of this study and the sample size needed to detect d = 0.3.
- Tested the treatment effect in 5 overlapping demographic subgroups, then applied Bonferroni and Benjamini-Hochberg corrections for multiple testing.
- Simulated p-value distributions when the null is true and when it is false.

## Key Findings

- Trainees earned $1,794 more than controls in 1978 (Welch's t = 2.674, p = 0.0079).
- Cohen's d was 0.2727, so the effect is statistically significant but small.
- Across the 5 subgroups, 2 effects were significant before correction. Only 1 stayed significant after Bonferroni correction.
- Testing several subgroups raises the chance of a false positive, which is why the corrections matter.
