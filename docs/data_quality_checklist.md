# Customer Churn Data Quality Checklist

Run these checks before interpreting churn rates. Confirm the source grain and field names before implementing them.

## 1. Population and keys
- [ ] Confirm whether one row represents one customer or a customer-period snapshot.
- [ ] Check customer identifiers for missing values and duplicates at the declared grain.
- [ ] Define the eligible customer population and observation window.
- [ ] Identify customers with unknown or missing churn status; do not silently classify them as retained.

## 2. Field checks
- [ ] Validate churn labels against the documented allowed values.
- [ ] Review missing values in tenure, charges, contract, payment, and service fields where present.
- [ ] Check numeric ranges and impossible values.
- [ ] Standardize category labels while preserving a record of transformations.

## 3. Metric definitions
- [ ] Define churn count and the eligible-population denominator.
- [ ] Calculate churn rate as churned eligible customers divided by eligible customers.
- [ ] For segment rates, show each segment's sample size.
- [ ] Document treatment of new customers, censored observations, and unknown statuses.

## 4. Interpretation
- [ ] Reconcile segment counts to the overall population.
- [ ] Separate descriptive association from causation.
- [ ] Do not infer a retention intervention's effect without a suitable experiment or design.
- [ ] Label synthetic practice data clearly and add findings only after reproducing the analysis.