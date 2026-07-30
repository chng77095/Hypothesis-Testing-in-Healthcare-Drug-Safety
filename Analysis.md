# Hypothesis Testing in Healthcare: Drug Safety

## Project Overview

Pharmaceutical drugs are an essential part of modern healthcare; however, ensuring their safety is critical before approval and widespread use. This project evaluates whether a hypothetical drug developed by **GlobalXYZ** produces adverse reactions that occur at statistically significant levels compared with a placebo.

GlobalXYZ completed a randomized controlled drug trial and provided the dataset for independent analysis. The goal of this analysis is to determine whether adverse effects observed in participants are associated with the experimental drug.

The dataset was obtained from **Hbiostat** courtesy of the Vanderbilt University Department of Biostatistics. It contains demographic information, vital signs, laboratory measurements, and adverse effect data.

The modified dataset contains the following variables:

| Column | Description |
|---|---|
| `sex` | Gender of the individual |
| `age` | Age of the individual |
| `week` | Week of drug testing |
| `trx` | Treatment group (Drug or Placebo) |
| `wbc` | White blood cell count |
| `rbc` | Red blood cell count |
| `adverse_effects` | Presence of at least one adverse effect |
| `num_effects` | Number of adverse effects experienced |

---

# Analysis 1: Proportion of Adverse Effects

## Statistical Test

A **two-proportion z-test** was performed to determine whether the proportion of participants experiencing at least one adverse effect differed between the **Drug** and **Placebo** groups.

## Hypotheses

- **Null Hypothesis (H₀):** The proportion of participants experiencing adverse effects is the same in the Drug and Placebo groups.
- **Alternative Hypothesis (H₁):** The proportion of participants experiencing adverse effects differs between the Drug and Placebo groups.

## Results

| Test | Result |
|---|---|
| Statistical Test | Two-Proportion Z-Test |
| p-value | **0.9639** |
| Significance Level (α) | **0.05** |

The p-value of **0.9639** is greater than the significance level of **0.05**. Therefore, we **fail to reject the null hypothesis**.

## Interpretation

The results indicate that there is **no statistically significant difference** in the proportion of participants experiencing adverse effects between the Drug and Placebo groups.

From a drug safety perspective, the experimental drug does **not appear to increase the likelihood of adverse effects** compared with the placebo. The observed differences between groups are likely due to random variation rather than the effect of the treatment.

---

# Analysis 2: Number of Adverse Effects

## Statistical Test

A **chi-square test of independence** was conducted to determine whether the number of adverse effects experienced by participants was associated with their assigned treatment group.

## Hypotheses

- **Null Hypothesis (H₀):** The number of adverse effects experienced is independent of treatment group.
- **Alternative Hypothesis (H₁):** The number of adverse effects experienced is associated with treatment group.

## Results

| Test | Result |
|---|---|
| Statistical Test | Chi-Square Test of Independence |
| p-value | **0.6150** |
| Significance Level (α) | **0.05** |

The p-value of **0.6150** is greater than **0.05**, meaning we **fail to reject the null hypothesis**.

## Interpretation

The analysis found **no statistically significant association** between treatment assignment and the number of adverse effects experienced by participants.

Participants receiving the experimental drug did not experience a significantly different number of adverse effects compared with participants receiving the placebo.

These findings suggest that the experimental drug does not increase the overall number of adverse reactions observed in the study population.

---

# Analysis 3: Age Differences Between Treatment Groups

## Statistical Test

A **Mann–Whitney U test** was performed to determine whether participant ages differed significantly between the Drug and Placebo groups.

The Mann–Whitney U test was selected because it is a non-parametric test that does not require the assumption of normally distributed data.

## Hypotheses

- **Null Hypothesis (H₀):** The age distributions of participants are the same between the Drug and Placebo groups.
- **Alternative Hypothesis (H₁):** The age distributions differ between the Drug and Placebo groups.

## Results

| Test | Result |
|---|---|
| Statistical Test | Mann–Whitney U Test |
| p-value | **0.2570** |
| Significance Level (α) | **0.05** |

The p-value of **0.2570** is greater than **0.05**, so we **fail to reject the null hypothesis**.

## Interpretation

The results indicate that there is **no statistically significant difference** in the age distributions of participants between the Drug and Placebo groups.

This suggests that randomization successfully created comparable treatment groups. Since age is similar between groups, it is unlikely to act as a confounding variable when evaluating the safety outcomes of the drug.

---

# Overall Conclusion

The goal of this analysis was to determine whether the experimental drug produced significantly different adverse effects compared with a placebo.

| Research Question | Statistical Test | p-value | Conclusion |
|---|---|---|---|
| Does the proportion of adverse effects differ? | Two-Proportion Z-Test | **0.9639** | No significant difference |
| Is the number of adverse effects associated with treatment? | Chi-Square Test | **0.6150** | No significant association |
| Are participant ages different between groups? | Mann–Whitney U Test | **0.2570** | No significant difference |

Overall, the hypothesis tests provide **no statistical evidence that the experimental drug increases adverse effects compared with the placebo**. Additionally, the treatment groups were comparable in age, supporting the validity of the randomized controlled trial.

Based on these findings, the experimental drug demonstrates a safety profile similar to the placebo with respect to the adverse effects analyzed.
