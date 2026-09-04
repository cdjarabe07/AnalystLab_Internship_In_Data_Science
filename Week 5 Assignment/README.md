# Week 5 – Baseline No-Show Model

Data preparation, feature engineering, and a first baseline model for predicting appointment
no-shows, building on the Week 4 problem definition.

## What was done

- Excluded Cancelled appointments, cleaned missing values, dropped `waiting_time_minutes` (data quality issue from Week 4)
- Engineered `prev_noshow_rate`, `has_history`, `lead_time_bucket`
- Split train/test by patient, not by row, to avoid leakage
- Trained a logistic regression baseline

## Result

ROC-AUC 0.677, accuracy 0.627. `booking_lead_days` and `previous_no_shows` were the strongest predictors.

## Files

- `notebooks/week5_baseline_model.ipynb`
- `reports/data_science_baseline_modelling_report.docx`
- `reports/week5_project_summary.docx`
- `visuals/`
