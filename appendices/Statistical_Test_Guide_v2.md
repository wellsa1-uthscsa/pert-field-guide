# Statistical Test Guide

*A practical decision aid for selecting common statistical approaches in clinical and population health research*

---

# Before Choosing a Statistical Test

Most statistical decisions become easier once three questions are answered:

### 1. What is my outcome?

- Continuous?
- Binary?
- Categorical?
- Time-to-event?

### 2. How many groups am I comparing?

- One group
- Two groups
- Three or more groups

### 3. What question am I trying to answer?

- Compare groups?
- Measure association?
- Predict outcomes?
- Estimate time-to-event risk?

Statistical tests should be chosen because they answer the scientific question, not because they are familiar.

---

# Quick Decision Tree

```text
Continuous outcome?
│
├─ Two groups
│   └─ t-test
│
├─ Three or more groups
│   └─ ANOVA
│
└─ Multiple predictors
    └─ Linear Regression

Binary outcome?
│
├─ Two categorical variables
│   └─ Chi-Square Test
│
└─ Multiple predictors
    └─ Logistic Regression

Time-to-event outcome?
│
├─ Group comparison
│   └─ Kaplan-Meier + Log-Rank Test
│
└─ Multiple predictors
    └─ Cox Regression
```

---

# Comparing Means

## One-Sample t-Test

### Use When

Comparing a sample mean against a known value.

### Example

Is the average PHQ-9 score different from a population benchmark?

---

## Independent Samples t-Test

### Use When

Comparing the means of two independent groups.

### Outcome Type

Continuous

### Example

Do participants with insomnia have higher depression scores than those without insomnia?

### Output

- Mean difference
- Confidence interval
- p-value

---

## Paired t-Test

### Use When

Comparing measurements collected from the same individuals at two time points.

### Example

Do depression scores improve after treatment?

---

## ANOVA

### Use When

Comparing means across three or more groups.

### Outcome Type

Continuous

### Example

Do depression scores differ across sleep-duration categories?

### Important

ANOVA indicates whether differences exist.

Post-hoc analyses identify where differences occur.

---

# Comparing Proportions

## Chi-Square Test

### Use When

Comparing categorical variables.

### Example

Is depression more common among individuals with insomnia?

### Variables

- Exposure: Insomnia (Yes/No)
- Outcome: Depression (Yes/No)

### Output

Tests whether proportions differ across groups.

---

## Fisher's Exact Test

### Use When

Cell counts are small.

### Example

Rare disease studies with limited sample sizes.

---

# Correlation

## Pearson Correlation

### Use When

Evaluating linear relationships between two continuous variables.

### Example

Relationship between sleep duration and depressive symptom scores.

### Output

Correlation coefficient (r)

Range:

- -1 = Perfect negative relationship
- 0 = No relationship
- +1 = Perfect positive relationship

---

## Spearman Correlation

### Use When

Variables are not normally distributed or relationships are monotonic rather than strictly linear.

### Example

Relationship between symptom severity rankings and functional impairment rankings.

---

# Linear Regression

## Purpose

Model a continuous outcome using one or more predictors.

### Outcome Type

Continuous

### Example

Predict depressive symptom score using:

- Age
- Sex
- Sleep duration
- Trauma exposure

### Advantages

Allows adjustment for potential confounders.

### Output

Regression coefficients describing expected changes in the outcome.

---

# Logistic Regression

## Purpose

Model a binary outcome.

### Outcome Type

Binary

Examples:

- Depression (Yes/No)
- Suicide attempt (Yes/No)
- Dementia diagnosis (Yes/No)

### Example

Does sleep disturbance predict depression after adjusting for age and sex?

### Output

Odds Ratios (ORs)

### Interpretation

OR = 1.5

Individuals with the exposure have 50% higher odds of the outcome.

---

# Survival Analysis

## Kaplan-Meier Curves

### Use When

Examining time-to-event outcomes.

### Example

Time from insomnia diagnosis to depression diagnosis.

### Output

Visual estimate of event probability over time.

---

## Log-Rank Test

### Use When

Comparing Kaplan-Meier curves.

### Example

Do exposed and unexposed groups experience different event rates over time?

---

## Cox Proportional Hazards Regression

### Use When

Modeling time-to-event outcomes while adjusting for covariates.

### Example

Does sleep disturbance predict future depression after adjusting for age, sex, and trauma?

### Output

Hazard Ratios (HRs)

### Interpretation

HR = 1.4

The outcome occurs approximately 40% faster in the exposed group.

---

# Common Epidemiologic Models

## Logistic Regression

Outcome:

- Disease present versus absent

Produces:

- Odds Ratios

---

## Cox Regression

Outcome:

- Time-to-event

Produces:

- Hazard Ratios

---

## Poisson Regression

Outcome:

- Counts or rates

Produces:

- Rate Ratios

---

## Linear Regression

Outcome:

- Continuous variable

Produces:

- Regression coefficients

---

# Confidence Intervals

Confidence intervals provide information about precision.

### Example

OR = 1.8

95% CI = 1.3–2.4

Interpretation:

The estimate suggests increased odds and the interval excludes the null value of 1.

### Narrow Intervals

Greater precision.

### Wide Intervals

Less precision.

---

# Statistical Significance

Researchers frequently use:

p < 0.05

as a threshold for statistical significance.

However, statistical significance should never be interpreted in isolation.

Always ask:

- Is the effect large?
- Is it clinically meaningful?
- Could bias explain the result?
- Does the finding fit existing evidence?

Statistical significance is one piece of evidence.

It is not the entire argument.

---

# Multiple Comparisons

The more tests performed, the greater the likelihood of false-positive findings.

Common approaches include:

- Bonferroni correction
- False Discovery Rate (FDR)
- Benjamini-Hochberg procedures

Whenever many outcomes are evaluated simultaneously, investigators should consider multiple-testing correction.

---

# Common Research Scenarios

## Scenario 1

Outcome:

Depression diagnosis (Yes/No)

Exposure:

Sleep disturbance

Suggested Analysis:

Logistic regression

---

## Scenario 2

Outcome:

PHQ-9 score

Exposure:

Trauma exposure

Suggested Analysis:

t-test or linear regression

---

## Scenario 3

Outcome:

Time to dementia diagnosis

Exposure:

Genetic variant

Suggested Analysis:

Cox proportional hazards regression

---

## Scenario 4

Outcome:

Depression prevalence

Exposure:

Sex

Suggested Analysis:

Chi-square test

---

# Questions to Ask Before Running Any Analysis

1. What is my outcome?
2. How is the outcome measured?
3. What assumptions does the method require?
4. What confounders should be considered?
5. Does the chosen test answer the scientific question?
6. How will results be interpreted?

Good analyses begin with good questions.

Statistics are tools for answering questions—not substitutes for them.

---

# The Most Important Rule

Do not begin by asking:

> Which statistical test should I use?

Begin by asking:

> What question am I trying to answer?

The appropriate statistical approach often becomes obvious once the scientific question is clearly defined.
