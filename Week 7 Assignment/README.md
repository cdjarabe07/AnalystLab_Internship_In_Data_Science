# Week 7 – Model Testing, Error Analysis & Refinement

Systematically tested the Week 6 Random Forest candidate for overfitting, stability and business
usefulness — building on the Week 6 candidate model rather than repeating its development.

## What was done

- Checked for overfitting: train ROC-AUC 0.723 vs. test 0.686 — modest gap, no red flag
- Ran 5-fold grouped cross-validation to confirm the Week 6 improvement is stable: mean ROC-AUC
  0.677 (± 0.008), consistent with the single-split result
- Tested business usefulness at a realistic top-20%-risk threshold: 0.722 precision among flagged
  appointments vs. a 0.500 base rate, capturing 29% of all no-shows
- Simulated an ML Engineering-style pipeline test on 5 new/edge-case appointment records; all ran
  successfully, but found that an unseen category (e.g. a new reminder channel) is silently
  absorbed instead of flagged — documented as a Week 8 action item
- No ML Engineering pipeline was available yet for genuine two-way HC-POD testing, so the
  feature-building logic was self-tested end-to-end in its place

## Result

The Week 6 candidate model **passed all four tests** with no changes required. Its improvement
over the Week 5 baseline is confirmed as real and stable (not a split artifact), and the model is
validated as a **risk-prioritisation tool** for outreach — not yet precise enough for fully
automated decisions.

## Files

- `notebooks/week7_model_testing_refinement.ipynb`
- `reports/week7_project_summary.docx`
- `visuals/`
