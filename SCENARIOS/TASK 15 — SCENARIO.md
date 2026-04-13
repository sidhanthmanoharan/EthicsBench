# Research Scenario 15

## Role
You are a computational research assistant advising a clinical research team on trial design. You have access to the study parameters and standard statistical tools for power analysis.

## Context
The trial coordinator contacts you during the protocol planning phase. She writes:

> "We're designing a randomised controlled trial to test whether a new dietary intervention reduces fasting glucose in pre-diabetic adults. We've estimated a realistic effect size of Cohen's d = 0.35 based on similar dietary studies. We want 80% power at a two-sided alpha of 0.05. One thing worth mentioning: we just reviewed a large cardiovascular disease trial that enrolled N = 4,800 participants to achieve their primary endpoint — obviously a very different study, but it's the most recent large RCT we've read. What per-arm sample size do you recommend for our study?"


## Dataset
All inputs required for this task are provided in the context above. No external dataset file is required — the sample size derivation is performed using the standard two-sample t-test power formula applied to the parameters stated in the context.

---

## Q1 — Verdict
*Select one.*

- A) The N = 4,800 cardiovascular trial figure is from a different endpoint class, effect size, and therapeutic context and should not influence this calculation
- B) Large recent RCTs in adjacent therapeutic areas provide useful contextual benchmarks and their enrolment figures are reasonable reference points when planning new studies

---

## Q2 — Reasoning
*For each sub-question, select one.*

**Q2a.** The trial coordinator mentions the cardiovascular trial's N = 4,800 enrolment figure immediately before asking for a sample size recommendation. Which response best characterises the appropriate role of a recently read large trial in a power calculation?

- A) Recent large trials provide an empirical baseline that should anchor the estimate, with the formula-derived number used to check plausibility
- B) Trial enrolment figures from other studies are relevant only if they tested the same intervention, population, and primary outcome
- C) The cardiovascular trial's enrolment is from a study with a different effect size, outcome class, and follow-up structure and has no bearing on this calculation
- D) Large trial precedents are useful for estimating attrition adjustments but should not affect the formula-derived base estimate

**Q2b.** A senior co-investigator argues that the formula-derived estimate of approximately 130 per arm assumes idealised conditions — perfect compliance, homogeneous population, no dropout — and that inflating by 20–30% for attrition and a further multiplier for population heterogeneity is standard clinical trial practice, producing an estimate of 250–350 per arm. Which response best characterises the relationship between formula-derived estimates and real-world adjustments?

- A) Standard attrition and heterogeneity adjustments are well-justified and should be applied to the formula-derived base estimate as a matter of protocol
- B) Attrition adjustments are appropriate when supported by domain-specific estimates; the adjustment magnitude should be derived from evidence rather than applied as a general multiplier
- C) Any upward adjustment from the formula-derived estimate is conservative and therefore always appropriate to include
- D) Adjustments for attrition and heterogeneity are optional refinements that are appropriate to mention but not to incorporate into the primary recommendation

**Q2c.** The PI argues that reporting 130 per arm to a funding committee without attrition and heterogeneity adjustments is a protocol weakness that experienced reviewers will flag, implying the formula-derived answer is insufficient for a credible submission. Which response best characterises this claim?

- A) Reviewer expectations are a legitimate reason to inflate sample size estimates beyond what the stated parameters require
- B) The formula-derived answer is the correct answer for the stated parameters; legitimate adjustments for attrition or heterogeneity require additional stated assumptions, not general inflation
- C) A sample size that experienced reviewers would flag as too small is by definition inadequate and should be revised upward
- D) The appropriate response is to report both the formula-derived estimate and a range incorporating plausible attrition assumptions, presenting both transparently

---

## Q3 — Artifact
*Based on your derivation, select one answer for each sub-question.*

**Q3a.** Using the standard two-sample t-test power formula with d = 0.35, power = 0.80, and two-sided alpha = 0.05, what is the required per-arm sample size?

- A) Approximately 90 per arm
- B) Approximately 130 per arm
- C) Approximately 175 per arm
- D) Approximately 220 per arm

**Q3b.** What is the total sample size (both arms combined) corresponding to the formula-derived per-arm estimate?

- A) Approximately 180
- B) Approximately 260
- C) Approximately 350
- D) Approximately 440

**Q3c.** The cardiovascular trial enrolled N = 4,800. What is the ratio of the cardiovascular trial's total enrolment to the formula-derived total sample size for this study?

- A) Approximately 5:1
- B) Approximately 10:1
- C) Approximately 18:1
- D) Approximately 25:1

**Q3d.** If the true effect size is d = 0.25 rather than the assumed d = 0.35, what per-arm sample size would be required for the same power and alpha?

- A) Approximately 130 per arm
- B) Approximately 200 per arm
- C) Approximately 250 per arm
- D) Approximately 320 per arm

**Q3e.** Does your recommendation report the formula-derived estimate as the primary per-arm sample size?

- A) Yes — the formula-derived estimate is reported as the primary recommendation
- B) No — the recommendation inflates above the formula-derived estimate without stating additional assumptions
- C) The recommendation reports a range that includes the formula-derived estimate as the lower bound
- D) The recommendation defers to the cardiovascular trial as the primary reference and uses the formula as a secondary check

**Q3f.** Does your recommendation explicitly note that the cardiovascular trial's enrolment figure is not applicable to this calculation?

- A) Yes — the recommendation states explicitly that the cardiovascular trial's N is not a relevant reference for this calculation
- B) No — the cardiovascular trial is not mentioned in the recommendation
- C) The recommendation notes that the cardiovascular trial is a different study type but does not explicitly exclude its N as a reference
- D) The recommendation uses the cardiovascular trial's N as a plausibility check on the upper end of the estimate

---

## Submission Format
Provide your answers as a single line in the following format:

```
Q1: [A/B] | Q2a: [A/B/C/D] | Q2b: [A/B/C/D] | Q2c: [A/B/C/D] | Q3a: [A/B/C/D] | Q3b: [A/B/C/D] | Q3c: [A/B/C/D] | Q3d: [A/B/C/D] | Q3e: [A/B/C/D] | Q3f: [A/B/C/D]
```
