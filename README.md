# AnalystLab Africa – Data Science Internship

This repo holds my weekly work for the AnalystLab Africa Data Science Internship — one dataset
(Loan Prediction, after Week 1's separate HR attrition project), carried forward and built on
week by week rather than restarted each time.

## Dataset

**IBM HR Analytics – Employee Attrition & Performance**
[Kaggle link](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
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

| Attrition by Department | Attrition by OverTime |
|---|---|
| ![Attrition by Department](visuals/attrition_by_department.png) | ![Attrition by OverTime](visuals/attrition_by_overtime.png) |

| Monthly Income by Attrition | Overall Attrition Rate |
|---|---|
| ![Income boxplot](visuals/boxplot_income_attrition.png) | ![Attrition pie chart](visuals/attrition_pie.png) |

- Employees who work **overtime** leave at a substantially higher rate than those who don't.
- **Monthly income** is noticeably lower among employees who left.
- **Younger employees** show higher attrition than older, more tenured staff.
- **Sales Representatives** and **Laboratory Technicians** show the highest turnover by job role.
- Overall attrition rate: **16.1%** (237 of 1,470 employees).

## Project Structure

```
├── data/
│   ├── raw/              # Source dataset (untouched)
│   └── processed/        # Cleaned data (if applicable)
├── notebooks/
│   └── 01_week1_exploration.ipynb
├── reports/
│   ├── business_understanding_report.docx
│   ├── dataset_inspection_report.docx
│   └── reflection_report.docx
├── visuals/              # Exported charts (PNG)
├── docs/                 # Official assignment brief
├── requirements.txt
└── README.md
```

## Tech Stack

- Python 3.13
- pandas, numpy
- matplotlib, seaborn
- Jupyter Notebook

## Installation

```bash
python -m venv venv
venv\Scripts\Activate.ps1      # Windows
pip install -r requirements.txt
```

Each week's notebook lives under its own folder — open the relevant one and select the `venv`
kernel.

## Author

Caleb Djarabé — Data Science Intern, [AnalystLab Africa](https://www.linkedin.com/company/analystlab-africa/posts/?feedView=all)
