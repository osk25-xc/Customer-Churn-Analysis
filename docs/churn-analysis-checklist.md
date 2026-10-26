# Customer Churn Analysis Checklist

## Data understanding

- Identify the unit of analysis (usually one row per customer at a defined snapshot date).
- Check duplicate customer IDs, missing values, invalid categories, and inconsistent data types.
- Confirm the business definition of churn and the observation window.
- Check whether the target label is available at prediction time; prevent target leakage.

## Exploratory analysis

- Calculate overall churn rate using a clearly defined denominator.
- Compare churn across contract type, tenure, product usage, and support activity where available.
- Report both counts and rates so small groups are not misread.
- Separate association from causation; segment differences do not prove a cause.

## Modeling and evaluation (if a model is included)

- Split data before fitting preprocessing steps.
- Use stratified splits when appropriate and keep a final holdout set.
- Compare with a simple baseline.
- For imbalanced churn labels, report precision, recall, F1, and ROC-AUC or PR-AUC as appropriate—not accuracy alone.
- Document threshold choice and business costs of false positives and false negatives.

## Final report

- State the dataset source and any synthetic/sample-data limitations.
- Include reproducible steps and library requirements.
- Tie recommendations to observed evidence and describe limitations.
- Never claim model performance until the notebook or script has actually been run.