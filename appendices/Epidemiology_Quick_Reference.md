# Epidemiology Quick Reference

*A concise guide to core concepts used throughout the PERT Field Guide*

---

# Study Designs

## Cross-Sectional Studies

**Question:** What is happening right now?

Exposure and outcome are measured at the same time.

### Strengths

* Fast
* Relatively inexpensive
* Useful for prevalence estimates
* Useful for hypothesis generation

### Limitations

* Temporality often unclear
* Vulnerable to reverse causation
* Limited causal inference

### Example

Is sleep disturbance associated with depression among medical students?

---

## Cohort Studies

**Question:** What happens over time?

Participants are grouped according to exposure status and followed for outcomes.

### Strengths

* Establishes temporality
* Multiple outcomes can be studied
* Stronger causal inference than cross-sectional studies

### Limitations

* Time consuming
* Expensive
* Loss to follow-up may occur

### Example

Do individuals with chronic insomnia experience increased future depression risk?

---

## Case-Control Studies

**Question:** What differs between people with and without an outcome?

Participants are selected according to outcome status.

### Strengths

* Efficient for rare outcomes
* Relatively inexpensive
* Useful for hypothesis generation

### Limitations

* Recall bias
* Selection bias
* Temporality may be difficult to establish

### Example

Did individuals with suicide attempts experience different childhood exposures than controls?

---

# Common Measures of Association

## Risk

The probability that an outcome occurs.

### Example

If 20 of 100 participants develop depression:

Risk = 20 / 100 = 20%

---

## Relative Risk (RR)

Compares risk between groups.

### Interpretation

* RR = 1 → No association
* RR > 1 → Increased risk
* RR < 1 → Decreased risk

### Example

RR = 2.0

Interpretation:

The exposed group experienced twice the risk of the outcome.

---

## Odds Ratio (OR)

Compares odds between groups.

Frequently used in case-control studies and logistic regression.

### Interpretation

* OR = 1 → No association
* OR > 1 → Increased odds
* OR < 1 → Decreased odds

### Example

OR = 1.8

Interpretation:

The odds of the outcome are 80% higher in the exposed group.

---

## Hazard Ratio (HR)

Compares event rates over time.

Frequently used in survival analysis.

### Interpretation

* HR = 1 → No difference
* HR > 1 → Faster occurrence
* HR < 1 → Slower occurrence

### Example

HR = 1.5

Interpretation:

The outcome occurs 50% faster in the exposed group.

---

# Confounding and Bias

One of the most important lessons in epidemiology is that associations do not automatically represent causal relationships. Many observed findings can be partially or completely explained by confounding, bias, measurement limitations, or alternative explanations. Experienced investigators develop the habit of actively searching for these possibilities before accepting a result at face value.

## Confounding

Confounding occurs when a third variable influences both the exposure and the outcome, creating or exaggerating an apparent association.

### Example

Childhood adversity may be associated with both sleep disturbance and depression.

An observed sleep-depression association may therefore be partially explained by childhood adversity.

### Key Question

Could another factor explain both the exposure and the outcome?

---

## Residual Confounding

Residual confounding refers to confounding that remains after statistical adjustment.

This may occur because:

* Important variables were never measured
* Variables were measured imperfectly
* Adjustment methods were incomplete
* Available data do not fully capture the underlying construct

### Example

A study adjusts for age and sex but lacks information about socioeconomic status.

Residual socioeconomic confounding may remain.

### Common in EHR Research

Many important psychiatric and social determinants are incompletely represented in electronic health records, including:

* Housing instability
* Social support
* Childhood adversity
* Educational attainment
* Neighborhood environment

Even after propensity score matching or multivariable adjustment, residual confounding often remains possible.

---

## Confounding by Indication

The reason a patient receives a treatment is related to their underlying risk profile.

### Example

Patients prescribed antipsychotic medications often have more severe psychiatric illness than patients who are not prescribed those medications.

Observed outcomes may reflect underlying illness severity rather than medication effects.

### Common in EHR Research

Particularly important in studies involving:

* Medications
* Surgical procedures
* Hospitalization
* Specialty referrals
* Intensive treatments

---

## Time-Varying Confounding

Confounders may change over time and may themselves be influenced by prior exposures.

### Example

Depression severity influences medication use, while medication use may influence future depression severity.

The relationship changes throughout follow-up.

### Common in Longitudinal Studies

Time-varying confounding becomes increasingly important when analyzing outcomes across extended follow-up periods.

---

## Selection Bias

Selection bias occurs when systematic differences influence who enters a study or who remains in a study.

### Example

Individuals with severe symptoms may be less likely to complete surveys.

The resulting sample may not accurately represent the target population.

---

## Ascertainment Bias

Some individuals are more likely than others to have diagnoses detected and recorded.

### Example

Patients with frequent healthcare utilization often accumulate more diagnoses simply because they interact with the healthcare system more often.

### Common in EHR Research

One of the most important sources of bias in EHR-based studies.

Differences in:

* Healthcare utilization
* Observation time
* Number of visits
* Access to care

can strongly influence observed disease prevalence.

---

## Surveillance Bias

A specific form of ascertainment bias.

Individuals who are monitored more closely are more likely to have outcomes detected.

### Example

Patients receiving frequent psychiatric evaluations may accumulate more psychiatric diagnoses than individuals receiving less intensive follow-up.

---

## Information Bias

Information bias occurs when measurement errors systematically affect study results.

### Examples

* Recall bias
* Documentation bias
* Diagnostic bias
* Interviewer bias
* Misclassification

---

## Documentation Bias

Electronic health records reflect what was documented rather than everything that occurred.

### Example

A patient may experience depression but never receive a diagnostic code.

### Common in EHR Research

The absence of documentation does not necessarily indicate the absence of disease.

---

## Diagnostic Bias

Different clinicians may classify similar presentations differently.

### Example

One clinician may diagnose generalized anxiety disorder.

Another may diagnose adjustment disorder.

A third may not assign a formal diagnosis.

The underlying clinical presentation may be similar despite different coding patterns.

---

## Referral Bias

Patients reaching specialty care may differ substantially from those who never receive specialty evaluation.

### Example

Patients treated in psychiatry clinics may represent more severe illness than psychiatric patients in the general population.

### Common in Health-System Research

Referral patterns can strongly influence observed associations.

---

## Reverse Causation

The outcome influences the exposure rather than the exposure influencing the outcome.

### Example

Depression may contribute to sleep disturbance rather than sleep disturbance causing depression.

### Key Question

Could the direction of the relationship be reversed?

---

## Survivorship Bias

Individuals who remain observable differ from those who do not.

### Example

Patients lost to follow-up may systematically differ from those who remain under observation.

### Common in Longitudinal Research

The observed sample may become increasingly non-representative over time.

---

## Immortal Time Bias

A period during which an outcome could not have occurred is incorrectly attributed to an exposure group.

### Example

Patients must survive long enough to receive a treatment.

This can make treatments appear more protective than they truly are.

### Common in EHR Research

Particularly important in retrospective treatment-effect studies.

---

## Missing Data Bias

Missing information is often systematic rather than random.

### Example

Patients with severe illness may be less likely to complete questionnaires or follow-up assessments.

### Common Sources

* Laboratory data
* Behavioral variables
* Social determinants
* Survey responses

---

# Common Threats in EHR Research

When interpreting EHR-derived findings, ask the following questions:

1. Could healthcare utilization explain the result?
2. Could differential diagnosis rates explain the result?
3. Could documentation practices explain the result?
4. Could referral patterns explain the result?
5. Could treatment indication explain the result?
6. Could observation time differ between groups?
7. Could missing data influence interpretation?
8. Could residual confounding remain despite matching or adjustment?

These questions are particularly important when evaluating studies conducted using TriNetX, electronic health records, claims databases, registries, and other real-world data sources.

---

# Key Concepts

## Exposure

The factor being investigated.

### Examples

* Trauma
* Sleep disturbance
* Smoking
* Exercise

---

## Outcome

The condition or event being studied.

### Examples

* Depression
* Cognitive decline
* Suicide attempt
* Mortality

---

## Mediator

A variable that helps explain how an exposure influences an outcome.

### Example

Childhood adversity → Sleep disturbance → Depression

---

## Collider

A variable influenced by both exposure and outcome.

Adjusting for colliders can introduce bias and create misleading associations.

### Example

If both depression and sleep disturbance increase healthcare utilization, restricting analysis to frequent healthcare users may unintentionally distort the observed association.

---

## Temporality

Exposure occurs before outcome.

Temporality is essential for causal interpretation.

---

# Validity and Reliability

## Reliability

Consistency of measurement.

### Question

Would repeated measurements produce similar results?

---

## Validity

Accuracy of measurement.

### Question

Does the variable capture the concept of interest?

---

## Misclassification

Participants are assigned to the wrong category.

### Examples

* False positive diagnoses
* False negative diagnoses
* Incorrect exposure classification

Misclassification may be random or systematic and can substantially influence results.

---

# Reading a Study

When evaluating a paper, ask:

1. What is the research question?
2. What study design was used?
3. How were exposure and outcome defined?
4. Could confounding explain the result?
5. Could bias explain the result?
6. Is temporality established?
7. Are conclusions justified by the evidence?
8. What alternative explanations remain plausible?

---

# Population Health Lens

When interpreting findings, ask:

* What upstream factors may contribute?
* Are social determinants considered?
* Are disparities present?
* Which populations are represented?
* Which populations may be missing?
* What larger systems may be influencing the observed pattern?

---

# The Five Questions of Epidemiologic Thinking

1. What am I trying to explain?
2. How am I measuring it?
3. Should I believe this result?
4. What alternative explanations exist?
5. Why does this pattern occur across populations?

These questions provide the intellectual foundation of the PERT Field Guide.
