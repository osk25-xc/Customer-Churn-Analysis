# Customer Churn Evaluation Plan

## Target definition
Document the exact churn label, observation window, and prediction cutoff. Remove records whose outcome would not yet be observable at the cutoff.

## Data preparation
Check customer ID uniqueness, missing target labels, leakage-prone fields, category consistency, and numeric ranges. Split train and test data before fitting preprocessing steps.

## Evaluation
Report confusion matrix, precision, recall, F1, and ROC-AUC where appropriate. For imbalanced churn classes, include the positive-class prevalence and avoid relying on accuracy alone. Choose a threshold using business costs rather than defaulting automatically to 0.5.

## Validation
Use a held-out test set or time-aware split when chronology matters. Compare against a simple baseline and inspect performance by relevant customer segments with adequate sample sizes.

## Caveats
A predictive association is not a causal retention lever. Do not claim model quality until the notebook is executed and metrics are recorded.
