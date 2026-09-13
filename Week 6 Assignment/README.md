# Week 6 – Model Improvement, Error Analysis & Validation

Diagnosed the weaknesses of the Week 5 baseline, engineered a new feature based on that
diagnosis, and compared candidate models — building on the Week 5 baseline model.

## What was done

- Reproduced and verified the Week 5 baseline (ROC-AUC 0.677, accuracy 0.627)
- Ran error analysis on the confusion matrix: 166 missed no-shows and 194 false alarms out of 966
  test cases
- Found the baseline over-relies on `booking_lead_days`: correctly-caught no-shows average ~44
  days lead time vs. only ~19 days for missed ones
- Engineered `leaddays_x_prevrate` (lead time × prior no-show rate) to capture that interaction
- Trained and compared three candidates (logistic regression + interaction, Random Forest,
  Gradient Boosting) on the same patient-level split
- Reached out to the Data Analytics track for cross-track input; no response by the deadline, so
  ran a DA-style segment analysis independently (distance, day, time, appointment type)
- Found reminders lose most of their effect for the farthest patients (-10 points no-show for
  mid-distance patients vs. only -2 points for the farthest) — tested as a model feature
  (`far_and_reminded`), which didn't improve the metric but stands as an operational insight

## Result

**Random Forest** is the best candidate: ROC-AUC 0.686, accuracy 0.636 — a real but modest
improvement over the baseline. `booking_lead_days` and `leaddays_x_prevrate` remain the strongest
predictors; `distance_to_clinic_km` also ranks high, explained in part by the reminder-effectiveness
finding above.

## Files

- `notebooks/week6_model_improvement_validation.ipynb`
- `reports/week6_project_summary.docx`
- `visuals/`
