# Week 7 - HealthConnect Experience Lab: Model Testing, Error Analysis & Refinement

**Track:** Data Science
**Project:** HealthConnect Clinic - Improving Patient Appointment Attendance and Healthcare Support Using Data and AI

## Overview

Week 7 moves the project from integration (Week 6) into **Testing → Refinement → End-to-End Validation**. The Week 6 candidate model is systematically tested, issues are identified and addressed where possible, refinements are re-tested, and a real HC-POD cross-track validation activity is completed with the Data Analytics track.

## Testing Summary

| # | Test | Result | Assessment |
|---|---|---|---|
| 1 | Patient-level split robustness check | 0.670 vs 0.682 (time-based) | Pass with caveat |
| 2 | Classification threshold tuning | Recall 66.5% → 97.5% at threshold 0.30 | Pass |
| 3 | Subgroup fairness - age | ROC-AUC 0.666–0.729 across 6 groups | Pass |
| 4 | Subgroup fairness - gender | 0.725 (male) vs 0.639 (female) | **Fail - issue identified** |
| 5 | Refinement re-test (gender interactions) | Gap essentially unchanged | **Fail - not adopted** |
| 6 | Statistical significance of Week 6 gain | Bootstrap 95% CI [0.002, 0.019] | Pass (marginal) |
| 7 | HC-POD cross-track alignment with Data Analytics | 98.3% overlap | Pass - validated |

## Key Outcomes

- **Validated performance estimate:** ROC-AUC ≈0.670 on genuinely unseen patients (patient-level split), confirming the Week 6 leakage concern was valid but modest.
- **Evidence-based operating recommendation:** threshold of **0.30–0.35** rather than the default 0.5, tuned to HealthConnect's real cost asymmetry (a missed no-show wastes a full slot; a false alarm costs only an extra reminder).
- **Cross-track validation:** 98.3% of the model's top-risk predictions fall within the Data Analytics track's independently-defined high-risk segments  directly answering a question they posed in their own Week 6 findings document.
- **Open issue documented honestly:** a gender fairness gap (~0.09 ROC-AUC) was discovered; an attempted refinement did **not** close it, so it is reported as unresolved rather than presented as fixed.

## Files

| File | Description |
|---|---|
| `HealthConnect_Model_Testing_Refinement.ipynb` | Main Week 7 output: 7 documented tests, refinement attempts, re-tests, cross-track validation |
| `Week7_Project_Summary.docx` | Concise summary of Week 7 work and proposed Week 8 focus |

## Next Steps (Week 8)

Final integration and presentation: frame the model honestly as a validated prioritisation aid with a documented fairness caveat and a proposed path forward; finalise the ML Engineering handover interface; align the narrative with the other HC-POD tracks.

---
*Part of the AnalystLab Africa Data Science Internship Programme — Batch D.*
