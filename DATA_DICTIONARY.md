# Customer Churn Dataset — Data Dictionary

The notebook creates and analyzes a practice dataset with 2,000 customer records and 12 columns. The dataset is synthetic and is intended for learning and portfolio demonstration.

| Column | Meaning | Type / example |
|---|---|---|
| `Customer_ID` | Unique customer identifier | Text, e.g. `CUST10000` |
| `Age` | Customer age | Integer |
| `Gender` | Recorded gender category | Category |
| `Tenure_Months` | Customer tenure in months | Integer |
| `Contract` | Contract type | Category, e.g. One Year |
| `Payment_Method` | Payment method | Category |
| `Internet_Service` | Internet service type | Category |
| `Subscription` | Subscription tier | Category |
| `Monthly_Charges` | Monthly billed amount | Decimal |
| `Total_Charges` | Total charges recorded | Decimal |
| `Support_Calls` | Number of support calls | Integer |
| `Churn` | Whether the customer churned | Yes/No category |

## Suggested validation before analysis

1. Confirm `Customer_ID` is unique.
2. Check that age, tenure, charges, and support calls are non-negative and within sensible business ranges.
3. Confirm `Churn` contains only the expected Yes/No labels.
4. Review category spelling and capitalization before grouping.
5. Calculate churn rate as churned customers divided by all eligible customers in the same analysis population.

## KPI definition

**Churn Rate (%)** = (Number of customers with `Churn = 'Yes'` / Total eligible customers) × 100.

State the population and observation period whenever reporting this metric. Do not interpret associations in this synthetic dataset as proof of causation.

## Reproducibility note

The notebook contains the dataset-generation and analysis workflow. Re-run the notebook from the top to regenerate outputs; verify the current notebook cells and file paths before comparing results.
