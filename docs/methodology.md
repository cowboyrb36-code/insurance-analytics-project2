📄 methodology.md — Project 2 Workflow
1. Project Overview
This project analyzes medical insurance charges to identify the strongest cost drivers across demographic, behavioral, and regional variables. The workflow follows a complete analytics lifecycle: data cleaning → SQL analysis → visualization → insights → documentation.

2. Data Source
File: insurance_with_bmi_category.csv

Rows: 1,338

Columns: age, sex, BMI, region, smoker status, charges, children

Engineered feature: BMI Category (Underweight, Normal, Overweight, Obese)

3. Data Cleaning (Excel + AI‑Assisted Validation)
Steps performed:
Verified column types (numeric vs. categorical)

Checked for missing values (none found)

Standardized categorical labels:

sex → male/female

smoker → True/False

region → northeast/northwest/southeast/southwest

Created BMI Category using Excel + AI‑assisted logic:

Underweight: BMI < 18.5

Normal: 18.5–24.9

Overweight: 25–29.9

Obese: ≥ 30

Why Excel first?
Excel is ideal for quick validation, spotting anomalies, and confirming data integrity before loading into SQL or Tableau.

4. SQL Analysis (BigQuery)
SQL was used to compute all grouped metrics used in Tableau:

Average charges by smoker status

Average charges by BMI category

Smoker × BMI heatmap

Gender × BMI category

Age group cost trends

Regional cost differences

Top 10 highest claims

All queries are stored in:

sql/analysis_queries.sql

This ensures the analysis is reproducible and transparent.

5. Feature Engineering
BMI Category
Created to allow categorical comparisons in Tableau.

Age Groups
Generated in SQL using CASE statements:

18–25

26–35

36–45

46–55

56–65

These groups align with common healthcare segmentation.

6. Visualization (Tableau)
A multi‑worksheet dashboard was created to visualize:

Smoker vs. Non‑Smoker charges

BMI category trends

Smoker × BMI heatmap

Gender × BMI category

Age group cost progression

Regional differences

The dashboard is published on Tableau Public.


Preview image stored in: tableau/dashboard_overview.png

7. Insight Generation (AI‑Assisted)
AI was used to:

Validate outliers

Summarize patterns

Compare demographic groups

Draft narrative insights

Ensure clarity and executive readability

All insights are documented in:

docs/insights_summary.md

8. Final Deliverables
README.md — Project overview

Dataset — /data/insurance_with_bmi_category.csv

SQL queries — /sql/analysis_queries.sql

Insights summary — /docs/insights_summary.md

Methodology — /docs/methodology.md

Dashboard assets — /tableau/

This structure mirrors real analytics team workflows and demonstrates end‑to‑end capability.
