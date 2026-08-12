# Employee Attrition Analysis — Week 1
**AnalystLab Africa | Data Science Internship Programme**
**Project:** Business Understanding & Data Exploration
**Client scenario:** ABC Manufacturing Ltd

## Overview

This project is the Week 1 deliverable of the AnalystLab Africa Data Science Internship Programme. Acting as a Junior Data Scientist for a consulting engagement with ABC Manufacturing Ltd, the goal is to understand *why* employees are leaving the company before any predictive machine learning model is built.

The work follows a Business Understanding → Data Exploration structure (aligned with CRISP-DM), using the **IBM HR Analytics – Employee Attrition & Performance** dataset (1,470 employees, 35 attributes).

## Business Questions Answered

1. What does the company's workforce look like?
2. Which departments have the highest employee attrition?
3. Does age influence attrition?
4. Does monthly income affect retention?
5. Does overtime influence attrition?
6. Which job roles experience the highest turnover?
7. Which variables appear important for future predictive modelling?

## Key Findings

- Overall attrition rate: **16.1%** (237 of 1,470 employees)
- Employees who work **overtime** leave at ~**3x** the rate of those who don't (30.5% vs 10.4%)
- **Sales Representatives** have the highest attrition by job role (39.8%)
- Median monthly income for employees who left is **38% lower** than for those who stayed
- **Sales** (20.6%) and **Human Resources** (19.0%) departments show the highest attrition; R&D the lowest (13.8%)
- Younger, single employees are more likely to leave than older, married employees

## Repository Structure

```
├── Employee_Attrition_Analysis.ipynb     # Main analysis notebook (EDA + visualisations)
├── data/
│   └── WA_Fn-UseC_-HR-Employee-Attrition.csv
├── reports/
│   ├── Business_Understanding_Report.docx
│   ├── Dataset_Inspection_Report.docx
│   └── Reflection_Report.docx
└── README.md
```

## Tools & Libraries

- Python 3
- Pandas — data loading & inspection
- Matplotlib / Seaborn — data visualisation
- Jupyter Notebook

## How to Run

```bash
git clone <this-repo-url>
cd employee-attrition-analysis
pip install pandas matplotlib seaborn notebook
jupyter notebook Employee_Attrition_Analysis.ipynb
```

Make sure the dataset CSV is in the same directory (or update the file path in the first code cell), then run all cells.

## Dataset Source

[IBM HR Analytics – Employee Attrition & Performance (Kaggle)](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)

## Author

Mairame Samba Niang — Data Science Intern, AnalystLab Africa | Senegal

---
*This project was completed as part of the AnalystLab Africa Data Science Internship Programme — Week 1 assignment.*
