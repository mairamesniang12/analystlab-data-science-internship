# Week 5 — HealthConnect Experience Lab: Data Preparation, Feature Engineering & Baseline Model

**Track:** Data Science
**Project:** HealthConnect Clinic — Improving Patient Appointment Attendance and Healthcare Support Using Data and AI

## Overview

Week 5 moves the HealthConnect Experience Lab from planning (Week 4) into practical implementation. Building directly on the Week 4 problem definition, this week prepares the appointment dataset for modelling, engineers new features, defines a leakage-aware train/test strategy, and trains and evaluates two baseline classification models.

## Data Science Track Contribution — Week 5

- **Data preparation:** handled missing values (median imputation for distance/waiting time; explicit "None" category for reminder_channel, since its missingness is informative, not random), validated data types, re-confirmed the Week 4 target definition.
- **Visual evidence:** 6 visualisations, each tied directly to a preparation, feature engineering, or modelling decision.
- **Feature engineering:** 5 new features (`no_show_rate_history`, `is_new_patient`, `long_lead_time`, `reminder_received`, `is_weekend_appointment`), each documented with rationale and expected value.
- **Train/test strategy:** a time-based (not random) 80/20 split, justified by realistic deployment simulation, with an explicitly documented trade-off around repeated patients.
- **Baseline models:** Logistic Regression (primary, for interpretability) and Random Forest (comparison), evaluated with accuracy, precision, recall, F1-score, confusion matrices, and ROC-AUC.
- **Cross-track collaboration:** aligned feature definitions with the Data Analytics track's proposed KPIs via the shared data dictionary.

## Key Findings

- Both baseline models achieve ROC-AUC ≈ 0.67-0.68 — meaningfully better than random guessing, but not yet a highly reliable predictor.
- Feature importance is led by `booking_lead_days`, `distance_to_clinic_km`, `age`, and `waiting_time_minutes` — a partially counter-intuitive result, since patient no-show history contributed less than the exploratory analysis alone suggested.
- The problem is confirmed **tractable but not easy** — a realistic, useful baseline finding for the HealthConnect project.

## Files

| File | Description |
|---|---|
| `HealthConnect_Baseline_Model.ipynb` | Main Week 5 output: data prep, feature engineering, train/test strategy, baseline models, evaluation |
| `Week5_Project_Summary.docx` | Concise summary of Week 5 work and proposed Week 6 focus |

## Next Steps (Week 6)

Hyperparameter tuning, a patient-level split robustness check, classification threshold tuning tied to real operational costs, and deeper feature engineering around distance and waiting time.

---
*Part of the AnalystLab Africa Data Science Internship Programme — Batch D.*
