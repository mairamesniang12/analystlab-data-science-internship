# Week 6 - HealthConnect Experience Lab: Model Improvement, Error Analysis & Validation

**Track:** Data Science
**Project:** HealthConnect Clinic - Improving Patient Appointment Attendance and Healthcare Support Using Data and AI

## Overview

Week 6 moves the HealthConnect project from initial implementation (Week 5) into integration, advanced development, and validation. This week's focus: analyse the weaknesses of the Week 5 baseline model, conduct error analysis, refine features with justified evidence, develop and compare an improved model, and complete a **real, evidence-based cross-track integration** with the Data Analytics track not just a conceptual dependency.

## Data Science Track Contribution - Week 6

- **Error analysis:** identified that the Week 5 model's False Negatives (missed no-shows) cluster among shorter booking lead times than the feature the model relies on most heavily.
- **Feature refinement:** engineered 3 new features (`mid_lead_time`, `distance_lead_interaction`, `high_risk_history`), each directly motivated by a specific error-analysis finding.
- **Model comparison:** trained and compared 3 improved candidates (tuned Random Forest, refined Logistic Regression, Gradient Boosting) against the Week 5 baseline.
- **Cross-track integration:** received a structured findings document from the Data Analytics track intern in my HealthConnect pod, independently validated all 4 of their quantitative findings on my own dataset, implemented and tested their 2 specific modelling suggestions (a categorical lead-time band feature and a `previous_no_shows × booking_lead_days` interaction term), and adopted both into the final candidate model after confirming a genuine performance improvement.
- **Structured feedback provided back to Data Analytics**, including a notable cross-track finding: previous no-show history is a strong *descriptive* signal in their analysis, but contributes less to the *predictive* model once other correlated variables are accounted for.

## Key Findings

- Feature refinement and model comparison produced a marginal improvement over the Week 5 baseline (ROC-AUC ≈0.672 → ≈0.680) an honest validation finding indicating a performance ceiling with the current feature set.
- Incorporating the Data Analytics-informed features pushed performance slightly further (≈0.680 → ≈0.682)  a small, genuine gain directly attributable to cross-track collaboration.
- All 4 Data Analytics findings (previous no-shows, lead-time bands, reminder status, distance) were independently replicated on this project's dataset, cross-validating both tracks' work.

## Files

| File | Description |
|---|---|
| `HealthConnect_Model_Improvement.ipynb` | Main Week 6 output: error analysis, feature refinement, model comparison, cross-track integration, candidate model |
| `Week6_Project_Summary.docx` | Concise summary of Week 6 work and proposed Week 7 focus |
| `Data_Analytics_Collaboration_with_Data_Science_track.pdf` | Findings document received from the Data Analytics track (cross-track integration evidence) |
| `DataScience_Feedback_to_DataAnalytics.docx` / `.pdf` | Structured feedback provided back to Data Analytics (cross-track integration evidence) |

## Next Steps (Week 7)

Patient-level split robustness check, classification threshold tuning tied to real operational costs, a basic subgroup fairness check, and finalising the handover interface for ML Engineering pipeline integration.

---
*Part of the AnalystLab Africa Data Science Internship Programme - Batch D.*
