# Week 1 – Employee Attrition Analysis (ABC Manufacturing Ltd)

AnalystLab Africa – Data Science Internship Programme
**Week 1: Business Understanding & Data Exploration**

## Overview

Exploratory data analysis on the IBM HR Analytics dataset (1,470 employees, 35 variables) to
understand the drivers of employee attrition for a fictional manufacturing client.

**Dataset:** [IBM HR Analytics – Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
1,470 employees · 35 variables · no missing values · no duplicate rows

## Business Questions Addressed

1. What does the company's workforce look like?
2. Which departments have the highest employee attrition?
3. Does age influence attrition?
4. Does monthly income affect retention?
5. Does overtime influence attrition?
6. Which job roles experience the highest turnover?
7. Which variables appear important for future predictive modelling?

## Key Findings

| Attrition by Department | Overall Attrition Rate |
|---|---|
| ![Attrition by Department](visuals/attrition_by_department.png) | ![Attrition pie chart](visuals/attrition_pie.png) |

- Employees who work **overtime** leave at a substantially higher rate than those who don't.
- **Monthly income** is noticeably lower among employees who left.
- **Younger employees** show higher attrition than older, more tenured staff.
- **Sales Representatives** and **Laboratory Technicians** show the highest turnover by job role.
- Overall attrition rate: **16.1%** (237 of 1,470 employees).

## Project Structure

```
├── data/raw/              # Source dataset
├── docs/                  # Official assignment brief
├── notebooks/
│   └── 01_week1_exploration.ipynb
├── reports/
│   ├── business_understanding_report.docx
│   ├── dataset_inspection_report.docx
│   └── reflection_report.docx
└── visuals/               # Exported charts (PNG)
```

## Deliverables

- [x] Business Understanding Report
- [x] Dataset Inspection Report
- [x] Reflection Report
- [x] Jupyter Notebook (EDA + visualisations)
- [x] GitHub Repository
- [x] LinkedIn Post
- [x] X Post
- [x] Google Drive Link Submitted
