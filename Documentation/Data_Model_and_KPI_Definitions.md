# Data Model and KPI Definitions

## 1. Purpose

This document describes the expected data grain, key fields, relationships and business KPI definitions for the Target Audience Analysis project.

The model will be validated against the original datasets before analytical joins and calculations are performed.

## 2. Dataset Grain

| Dataset | Expected Grain | Key Field |
|---|---|---|
| Customers | One record per customer | cust_id |
| Credit Profiles | To be validated | cust_id |
| Transactions | One record per transaction | tran_id |
| Campaign Dataset | To be inspected | To be determined |

## 3. Key Fields

### Customers
- cust_id: Customer identifier
- age: Customer age
- occupation: Customer occupation
- annual_income: Annual income
- location: Customer location

### Credit Profiles
- cust_id: Customer identifier
- credit_score: Credit score
- credit_utilisation: Credit utilisation
- outstanding_debt: Outstanding debt
- credit_limit: Credit limit

### Transactions
- tran_id: Transaction identifier
- cust_id: Customer identifier
- tran_date: Transaction date
- tran_amount: Transaction amount
- product_category: Transaction category
- platform: Transaction platform
- payment_type: Payment method

## 4. Expected Relationships

### Customers to Transactions
Expected relationship: One-to-many.

One customer may have multiple transactions.

Join key: cust_id.

### Customers to Credit Profiles
Relationship: Pending validation.

We must investigate whether each customer has exactly one credit profile or multiple profile records.

Join key: cust_id.

### Campaign Dataset
The dataset structure and relationship must be inspected before integration.

## 5. KPI Definitions

| KPI | Proposed Calculation |
|---|---|
| Total Customers | Distinct valid customer IDs |
| Total Transactions | Count of distinct transaction IDs |
| Total Transaction Value | Sum of valid transaction amounts |
| Average Transaction Value | Total transaction value / transaction count |
| Active Transacting Customers | Distinct customers with valid transactions |
| Transactions per Active Customer | Transaction count / active transacting customers |
| Average Annual Income | Average of valid customer income |
| Customer Distribution | Customer count by selected segment |
| Segment Spending Contribution | Segment transaction value / overall transaction value × 100 |
| Monthly Transaction Value | Sum of transaction value grouped by month |

## 6. Important Calculation Rules

- Customer counts must use distinct customer identifiers.
- Transaction counts must use distinct transaction identifiers.
- Transaction amounts must be validated before aggregation.
- Missing customer IDs must be investigated before joins.
- Average income must not treat missing income as zero.
- Currency units must be verified from dataset documentation before presenting monetary values.
- All KPIs must be calculated at the appropriate data grain.

## 7. Validation Status

The definitions above are proposed analytical rules.

Primary keys, duplicate records, referential integrity and relationship cardinalities must be tested before the final model is approved.

## 8. Initial Data Validation Results

| Dataset | Rows | Unique IDs | Duplicate ID Occurrences |
|---|---:|---:|---:|
| Customers | 1,000 | 1,000 | 0 |
| Credit Profiles | 1,004 | 1,000 | 4 |
| Transactions | 500,000 | 500,000 | 0 |

### Initial Observations

1. Customer identifiers are unique in the Customers dataset.
2. Credit Profiles contains four duplicate customer ID occurrences.
3. Transaction identifiers are unique in the Transactions dataset.
4. The campaign dataset contains 62 records and three columns.

### Pending Validation

- Investigate duplicate credit profile records.
- Check unmatched customer IDs.
- Validate missing identifiers.
- Inspect campaign date and metric quality.
- Confirm the grain of the campaign dataset.

These are initial validation results, not final data-quality approval.
