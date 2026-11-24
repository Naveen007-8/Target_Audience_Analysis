# Target Audience Analysis
## Data-Driven Credit Card Customer Acquisition Strategy

**Project Status:** In Progress  
**Domain:** Banking and Financial Services (BFSI)  
**Project Type:** End-to-End Data Analytics

---

## 1. Project Overview

This project aims to analyse customer demographics, income, occupational profiles, credit characteristics and transaction behaviour to identify promising customer segments for credit card marketing.

The objective is to help a bank understand its customer base, identify potential target audiences and develop evidence-based customer acquisition strategies in a competitive banking market.

The project uses Python, SQL and Power BI to transform raw customer and transaction data into meaningful business insights.

## 2. Real-World Business Problem

Banks operate in a competitive credit card market where customers receive different offers involving cashback, rewards, discounts, annual fees and other benefits.

A bank needs to understand which customer profiles demonstrate promising spending behaviour and which customer segments should be investigated further by its marketing team.

This project addresses the following business challenge:

**How can a bank use customer and transaction data to identify promising target audiences and improve its credit card marketing strategy?**

## 3. Project Objectives

- Analyse customer distribution across different age categories.
- Understand annual income patterns across occupations.
- Examine customer spending behaviour and transaction frequency.
- Analyse credit profiles and their relationship with customer characteristics.
- Identify customer segments with promising spending patterns.
- Understand product-category preferences across customer segments.
- Develop data-driven customer acquisition recommendations.
- Present findings through interactive Power BI dashboards.

## 4. Datasets

The project currently contains four source CSV files.

| Dataset | Description |
|---|---|
| customers.csv | Customer demographics, age, occupation, income and location |
| credit_profiles.csv | Credit scores, credit utilisation, outstanding debt and credit limits |
| transactions.csv | Customer transactions, dates, amounts, platforms and product categories |
| avg_transactions_after_campaign.csv | Daily average transaction metrics for test and control groups |

Initial dataset sizes:

| Dataset | Rows |
|---|---:|
| Customers | 1,000 |
| Credit Profiles | 1,004 |
| Transactions | 500,000 |
| Campaign | 62 |

Dataset quality, relationships and suitability for analysis are being validated.

## 5. Technology Stack

| Technology | Purpose |
|---|---|
| Python | Data analysis and processing |
| Pandas | Data cleaning and transformation |
| NumPy | Numerical operations |
| Matplotlib / Seaborn | Exploratory data visualisation |
| SQL / Oracle SQL | Business data analysis |
| Microsoft Power BI | Interactive dashboards |
| DAX | KPI calculations and measures |
| Excel | Data inspection and reporting |
| Git and GitHub | Version control and portfolio publication |

## 6. Project Workflow

1. Business Understanding
2. Data Understanding and Profiling
3. Data Quality Assessment
4. Data Cleaning
5. Data Transformation
6. Feature Engineering
7. Exploratory Data Analysis
8. SQL Business Analysis
9. Customer Segmentation
10. Power BI Dashboard Development
11. Business Recommendations
12. Final Reporting and Documentation

## 7. Key Business Questions

- Which age categories have promising spending behaviour?
- Which occupations demonstrate higher average annual income?
- Which income groups contribute the most transaction value?
- Which product categories are popular among different customer segments?
- How do spending patterns differ across locations?
- Which customer profiles should the marketing team investigate?
- What additional information is required to evaluate competitor positioning and campaign effectiveness?

## 8. Planned Dashboard

The Power BI report is planned to contain three pages:

1. Executive Overview
2. Customer Segmentation
3. Credit Card Acquisition Strategy

Dashboard screenshots and verified findings will be added after development.

## 9. Project Structure

```text
Target_Audience_Analysis/
│
├── Data/
│   └── Raw_Data/
│
├── Documentation/
│   ├── Business_Requirements.md
│   └── Data_Model_and_KPI_Definitions.md
│
├── Notebooks/
│   └── 01_Data_Profiling.ipynb
│
├── Python/
├── SQL/
├── PowerBI/
├── Images/
├── Reports/
├── Github/
│
├── README.md
├── requirements.txt
└── .gitignore
```

The structure and deliverables will be expanded as the project progresses.

## 10. Current Data Quality Observations

Initial validation identified:

- 1,000 unique customer IDs in the customer dataset.
- Four duplicated customer IDs in the credit-profile dataset.
- 500,000 unique transaction IDs.
- No unmatched non-null customer IDs in the initial relationship checks.
- A campaign dataset containing 62 daily observations.

These observations are preliminary. Further profiling and investigation are required before final cleaning decisions.

## 11. Important Limitations

The available data does not directly identify competitor bank relationships, existing credit card ownership, marketing conversion outcomes or customer acquisition costs.

Therefore, the project will identify promising customer segments based on observed characteristics and transaction behaviour.

It will not claim confirmed competitor market share, actual marketing ROI or individual credit card purchase probabilities without additional validated data.

## 12. Final Deliverables

Planned deliverables include:

- Python analysis notebooks
- Cleaned and transformed datasets
- Feature engineering documentation
- SQL business analysis scripts
- Customer segmentation findings
- Power BI dashboard
- Business recommendations
- Executive report
- Data dictionary and data quality documentation

## 13. Project Completion Target

**Target Completion Date: 9 December 2026**

The repository will be updated throughout the project with reproducible analysis, documented methodology and verified business findings.
