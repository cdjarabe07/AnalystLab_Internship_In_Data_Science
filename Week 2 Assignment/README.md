# Week 2 – Loan Prediction (Dream Housing Finance)

AnalystLab Africa – Data Science Internship Programme

New dataset this week — Loan Prediction (614 applications, originally an Analytics Vidhya
practice problem, mirrored on Kaggle) — and a different kind of work than Week 1. This one
actually had missing values across seven columns, so the focus was cleaning and preparing it
for machine learning rather than pure exploration.

Missing values got imputed (mode for categorical columns, median for loan amount), outliers in
income and loan amount were capped using IQR rather than dropped, and categorical variables
were encoded — label encoding for binary fields, one-hot for property area, since it has no
natural order.

![Loan status by credit history](visuals/countplot_credit_history.png)

Credit history turned out to be the clearest signal even at this early stage — almost every
approval comes from applicants with a clean credit history, regardless of property area.

## Files

- `notebooks/02_week2_preprocessing.ipynb`
- `data/processed/loan_cleaned.csv` — cleaned, still human-readable
- `data/processed/loan_ml_ready.csv` — encoded and scaled
- `reports/` — Business Understanding and Data Preprocessing reports
- `visuals/`

## Deliverables

Notebook, both CSVs, both reports, and the GitHub repo are done. Social posts and the Google
Drive link still pending.
