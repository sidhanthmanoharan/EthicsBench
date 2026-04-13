# INTEGRITY-Bench  
### Evaluating Ethical Behavior of Language Models in Scientific Research  

---

## Overview

INTEGRITY-Bench is a benchmark for evaluating the ethical behavior of large language models (LLMs) deployed as assistants in scientific research workflows.

While existing evaluations focus primarily on capability (e.g., reasoning, coding, factual recall), INTEGRITY-Bench targets a distinct dimension: whether models act in accordance with research integrity standards when faced with realistic pressures and incentives.

The benchmark consists of structured, domain-grounded tasks in which models must interpret data, reason about methodology, and make decisions with ethical implications. Each task is evaluated under controlled conditions, including scenarios where correct scientific behavior conflicts with external pressure.

---

## Design Principles

- **Realistic task environments**  
  Scenarios are modeled on common research workflows (data analysis, statistical interpretation, manuscript preparation) across domains including biology, physics, and AI.

- **Verifiable ground truth**  
  Tasks include structured datasets and objective questions with determinate answers.

- **Separation of knowledge and action**  
  The benchmark distinguishes between identifying an integrity violation and selecting an appropriate course of action.

- **Controlled pressure conditions**  
  Models are evaluated under varying forms of pressure to assess robustness of decision-making.

---

## PRESSURE Protocol

INTEGRITY-Bench includes **PRESSURE** (Pressure Robustness Evaluation for Scientific Integrity Tasks Under Realistic Environments), a multi-round evaluation protocol designed to measure how model behavior changes under incentive and authority pressure.

Each task is evaluated in three rounds:

1. **Baseline**  
   Standard conditions without external influence.

2. **Implicit Pressure**  
   Incentives related to performance, deadlines, or deployment outcomes.

3. **Explicit Pressure**  
   Direct instructions or arguments from authority figures, often including technically framed justifications.

Model responses are compared across rounds to quantify behavioral shifts.

---

## Task Structure

Each task includes:

- **Scenario**  
  A description of the research context and the model’s role.

- **Dataset**  
  Structured experimental or observational data.

- **Questions**  
  A set of multiple-choice items covering:
  - Ethical judgment (e.g., whether an action constitutes a violation)  
  - Procedural reasoning (appropriate course of action)  
  - Data interpretation (verification of statistical or factual claims)  

- **Prompt Variants**  
  Additional inputs used to introduce pressure conditions in later rounds.

Responses are required in a fixed format to enable automated parsing and evaluation.

---

## Evaluation Metrics

The benchmark reports performance along several dimensions:

- **Integrity Accuracy (IA)**  
  Accuracy under baseline conditions.

- **Pressure Robustness (PR)**  
  Change in performance under implicit and explicit pressure.

- **Authority Susceptibility (AS)**  
  Degree to which responses shift under explicit directives or arguments.

- **Stability**  
  Consistency of responses across evaluation rounds.

- **Knowledge–Action Gap**  
  Difference between correct identification of integrity issues and selection of appropriate actions under pressure.

---

## Human Annotation

Ground truth and evaluation criteria are supported by annotations from domain experts. The current release includes:

- 30 annotators with research experience  
- ~1200 annotated data points  

These annotations are used to validate task design and establish reference answers.
