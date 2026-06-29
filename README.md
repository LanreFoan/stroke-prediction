# Stroke Risk Prediction — Healthcare Dataset

### Project Guide for Students & Analysts

---

## Problem Statement

 Hospitals see thousands of patients annually with undetected stroke risk. Without early identification, strokes remain one of the leading causes of disability and death. This project answers:

> **"Which patients are at highest risk of stroke, and what can hospitals do about it — today?"**

---

## Dataset Overview

| Feature | Type | Notes |
|---|---|---|
| id | ID | Unique patient identifier |
| gender | Categorical | Male / Female / Other |
| age | Numeric | Continuous |
| hypertension | Binary | 0 = No, 1 = Yes |
| heart_disease | Binary | 0 = No, 1 = Yes |
| ever_married | Categorical | Yes / No |
| work_type | Categorical | 5 categories |
| Residence_type | Categorical | Urban / Rural |
| avg_glucose_level | Numeric | mg/dL |
| bmi | Numeric | Body mass index |
| smoking_status | Categorical | 4 categories |
| stroke | Binary (target) | 0 = No, 1 = Yes |

**New engineered columns (added in cleaning):**
- `age_group` — Binned age cohorts
- `glucose_tier` — Normal / Pre-diabetic / Diabetic / High Diabetic
- `bmi_category` — Underweight / Normal / Overweight / Obese

---

## Project Objectives & How Each Is Met

| # | Objective | How It's Addressed |
|---|---|---|
| 1 | Real-world problem | Stroke early-warning for Nigerian hospitals |
| 2 | Analyze with data | EDA across 12 features, 5 chart groups |
| 3 | Clean & transform | BMI imputation, age bins, glucose tiers, risk scoring |
| 4 | Trends & patterns | Age curves, city maps, comorbidity matrix |
| 5 | Actionable insights | Clinical recommendations |

---

## Key Findings

### Finding 1 — Age is the dominant predictor
Stroke rate climbs sharply after age 60. Patients 75+ have over 5× the stroke risk of those under 45. Hospitals should implement mandatory annual stroke assessments for all patients over 60.

### Finding 2 — Hypertension + Heart Disease is the deadliest combination
Patients with both conditions have a stroke rate 3–5× higher than patients with neither. This comorbidity pair is an immediate clinical red flag.

### Finding 3 — Elevated glucose is an independent risk factor
Patients with glucose > 140 mg/dL (diabetic tier) show significantly elevated stroke rates even after controlling for age. Diabetic patients need to be co-managed with neurology/cardiology teams.

### Finding 4 — Work type predicts access to care
Self-employed and Private sector workers have higher stroke rates, likely driven by delayed care-seeking and stress. Govt_job workers — who have health insurance access — have lower rates.



---

## Recommendations

### For Hospital Management
1. **Embed the risk scoring card into existing triage intake forms** — zero cost, immediate impact
2. **Flag patients with hypertension + heart disease** as automatic high-priority in the EMR system
3. **Create a stroke prevention outpatient clinic** targeting 60+ patients with quarterly follow-ups

### For Specialist Clinicians
1. **Co-manage diabetic patients** (glucose > 140) with neurology; glycaemic control reduces stroke risk
2. **Prioritise rural patients** who present — they likely delayed care longer and arrive at higher risk

### For Policy / Administration
1. **Expand workplace health programmes** targeting private sector and self-employed workers
2. **Use city-level stroke burden data** to allocate specialist staffing to highest-burden locations
