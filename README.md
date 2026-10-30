# Banking Loan & Transaction Analytics

An end-to-end banking analytics project focused on understanding **loan
portfolio performance** and **credit/debit transaction behaviour** using
SQL, Microsoft Excel, Power BI, and Tableau.

The project transforms structured banking data into business-focused
KPIs, analytical queries, and interactive dashboards that can support
reporting, performance monitoring, and management decision-making.

------------------------------------------------------------------------

## Project Overview

The project is organised into two analytical modules:

### 1. Banking Loan Analytics

This module analyses loan and customer-related information to understand
lending activity, repayment performance, and portfolio risk.

**Key areas analysed** - Customer and active-loan counts - Loan amount,
funded amount, and average loan size - Loan growth over selected
periods - Principal recovery and repayment behaviour - Interest income -
Delinquency and default indicators - Branch-wise loan distribution and
performance categories - Product-wise loan volume and interest income

**Example KPIs** - Total loan amount - Total funded amount - Average
loan size - Principal recovery rate - Delinquency rate - Default rate -
On-time repayment percentage - Interest income

### 2. Credit/Debit Transaction Analytics

This module analyses transaction-level records to understand account
activity, transaction flows, channel usage, and branch-level trends.

**Key areas analysed** - Total credit and debit amounts -
Credit-to-debit ratio - Net transaction amount (credit less debit) -
Daily, weekly, and monthly transaction volumes - Branch-wise transaction
values - Bank-wise transaction values - Transaction-method
distribution - Month-on-month branch transaction growth - Rule-based
identification of high-value transactions

**Example KPIs** - Total credit amount - Total debit amount -
Credit-to-debit ratio - Net transaction amount - Transaction count by
period - Branch-wise transaction volume - High-value transaction count

> **Note:** The high-value transaction flag in the SQL analysis uses a
> predefined amount threshold (greater than 4,500 in the dataset's
> amount units). It is a basic rule-based flag for further review, not a
> validated fraud-detection model. A high-value transaction is not
> necessarily fraudulent.

------------------------------------------------------------------------

## Tools & Technologies

  -----------------------------------------------------------------------
  Tool                                Usage
  ----------------------------------- -----------------------------------
  **MySQL**                           Data exploration, data-type
                                      standardisation, KPI calculations,
                                      aggregation, and business analysis

  **Microsoft Excel**                 Summary reporting, PivotTables,
                                      PivotCharts, and dashboarding

  **Power BI**                        Interactive dashboards, KPI cards,
                                      filters, and drill-through
                                      reporting

  **Tableau**                         Interactive visual analysis and
                                      dashboard development
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Data Overview

The project works with two structured datasets.

### Banking Loan Dataset

The loan analysis uses fields such as:

-   Client and account identifiers
-   Loan amount and funded amount
-   Disbursement date and loan status
-   Customer age group and employment type
-   Credit score and interest rate
-   Branch and product information
-   Total payments and principal recovered
-   Delinquency/default indicators
-   Repayment behaviour

### Credit/Debit Transaction Dataset

The transaction analysis uses fields such as:

-   Customer and account identifiers
-   Transaction date and transaction type
-   Transaction amount and recorded balance
-   Transaction description
-   Branch and bank name
-   Transaction method and currency

The availability of individual fields may vary by dataset or dashboard.

------------------------------------------------------------------------

## SQL Analysis

The repository contains separate SQL scripts for the two analytical
modules:

-   `BankingAnalytics.sql` --- loan portfolio and repayment analysis
-   `CreditDebitBankData.sql` --- credit/debit transaction analysis

SQL techniques demonstrated include:

-   `SELECT`, `WHERE`, `ORDER BY`, and `GROUP BY`
-   Aggregate functions such as `SUM()`, `AVG()`, and `COUNT()`
-   `COUNT(DISTINCT ...)` for unique-entity counts
-   Conditional aggregation with `CASE WHEN`
-   Date formatting and period-based aggregation
-   Common Table Expressions (CTEs)
-   Window functions, including `LAG()`
-   Schema and data-type standardisation using `ALTER TABLE`

The scripts include analytical queries for customer counts, loan
metrics, repayment indicators, branch/product comparisons, transaction
totals, and monthly growth.

------------------------------------------------------------------------

## Dashboards & Project Files

The project includes dashboard and analysis files in multiple formats:

  -------------------------------------------------------------------------------
  File / Folder                               Description
  ------------------------------------------- -----------------------------------
  `1st banking dashboard.pbix`                Banking dashboard

  `2nd banking dashboard.pbix`                Additional banking dashboard

  `CreditDebitBankDashboard.pbix`             Credit/debit transaction dashboard

  `Bank Analytics.twbx`                       Tableau packaged workbook

  `Twb_Debit Credit Tableau Dashboard.twbx`   Tableau credit/debit dashboard

  `DB1 Banking Excel.xlsx`                    Banking Excel workbook

  `DB2 Credit Debit Excel.xlsx`               Credit/debit Excel workbook

  `BankingAnalytics.sql`                      Loan analytics SQL queries

  `CreditDebitBankData.sql`                   Transaction analytics SQL queries

  `BANKING_ANALYTICS...pptx`                  Project presentation

  `images/`                                   Dashboard screenshots and
                                              supporting visuals

### Dashboard Screenshot Files

The `images/` folder contains these PNG screenshots:

- `Excel DB1.png` — Banking loan analytics Excel dashboard
- `Excel DB2.png` — Credit/debit transaction analytics Excel dashboard
- `PowerBI DB 1(1).png` — Banking analytics Power BI dashboard, screenshot 1
- `PowerBI DB 1(2).png` — Banking analytics Power BI dashboard, screenshot 2
- `PowerBI DB2(1).png` — Credit/debit analytics Power BI dashboard, screenshot 1
- `PowerBI DB2(2).png` — Credit/debit analytics Power BI dashboard, screenshot 2
- `Tableau DB1.png` — Banking analytics Tableau dashboard
- `Tableau DB 2.png` — Credit/debit analytics Tableau dashboard
  -------------------------------------------------------------------------------

------------------------------------------------------------------------

## Dashboard Gallery

The screenshots below are embedded directly in this README. Keep the image files in the repository's `images/` folder with the exact filenames shown.

### Excel Dashboards

**Banking Loan Analytics**

![Excel DB1 – Banking Loan Analytics](images/Excel%20DB1.png)

**Credit/Debit Transaction Analytics**

![Excel DB2 – Credit Debit Transaction Analytics](images/Excel%20DB2.png)

### Power BI Dashboards

**Banking Analytics – Dashboard 1**

![Power BI Banking Dashboard 1](images/PowerBI%20DB%201%281%29.png)

**Banking Analytics – Dashboard 2**

![Power BI Banking Dashboard 2](images/PowerBI%20DB%201%282%29.png)

**Credit/Debit Analytics – Dashboard 1**

![Power BI Credit Debit Dashboard 1](images/PowerBI%20DB2%281%29.png)

**Credit/Debit Analytics – Dashboard 2**

![Power BI Credit Debit Dashboard 2](images/PowerBI%20DB2%282%29.png)

### Tableau Dashboards

**Banking Analytics**

![Tableau Banking Dashboard](images/Tableau%20DB1.png)

**Credit/Debit Transaction Analytics**

![Tableau Credit Debit Dashboard](images/Tableau%20DB%202.png)

---

## Business Insights & Applications

The analysis is designed to help users explore questions such as:

-   Which loan products contribute the highest loan volume?
-   How is lending distributed across branches?
-   What do repayment, delinquency, and default indicators show?
-   Which branches record higher transaction values?
-   How do credit and debit values compare?
-   Which transaction methods are used most frequently?
-   How does transaction activity change month over month?
-   Which high-value transactions may warrant additional review?

These insights can support loan portfolio monitoring, operational
reporting, branch performance reviews, and further investigation of
unusual transaction patterns.

------------------------------------------------------------------------

## Data Preparation & Challenges

The project documentation identifies data preparation challenges
including:

-   Inconsistent date formats
-   Missing values
-   Inconsistent transaction descriptions
-   Data-type standardisation
-   Outliers in loan and transaction amounts
-   Standardising branch and customer-related fields
-   Maintaining dashboard performance with multiple filters and visuals

Data validation is important when comparing SQL outputs with dashboard
KPIs. Counts, date ranges, filters, aggregation levels, and calculation
definitions should be consistent across reports.

------------------------------------------------------------------------

## How to Explore the Project

1.  Clone or download this repository.
2.  Open the relevant `.sql` file in MySQL Workbench or another
    compatible MySQL client.
3.  Create or select the database and load the corresponding source
    tables before running the queries.
4.  Open the Excel workbooks to explore the summary reports.
5.  Open the `.pbix` files in Power BI Desktop.
6.  Open the `.twbx` files in Tableau Desktop or Tableau Reader.
7.  Refer to the project presentation and `images/` folder for an
    overview of the dashboards.

**Important:** The SQL scripts expect source tables with the names
referenced in the queries (including `final_fact_cleaned` and
`credit_debit_bank`). Load and validate the required tables before
executing the scripts. Some dashboard files may also depend on their
original data-source paths; reconnect the data sources if prompted.

------------------------------------------------------------------------

## Future Enhancements

Potential next steps include:

-   Automating data ingestion and scheduled refreshes
-   Building a documented ETL pipeline with data-quality checks
-   Developing predictive models for loan default and delinquency risk
-   Enhancing transaction monitoring with multiple risk signals and
    validated alert rules
-   Creating customer segmentation for portfolio analysis
-   Adding role-based dashboard access for business users
-   Publishing dashboards through a secure reporting environment

These are proposed enhancements and are not represented as completed
project features.

------------------------------------------------------------------------

## Important Notes & Metric Definitions

-   Dashboard figures should be interpreted using the units and filters
    of their underlying datasets.
-   A transaction credit/debit ratio compares transaction values; it
    does not, by itself, measure bank profitability or liquidity.
-   A delinquency indicator and a loan-default indicator are distinct
    classifications. Their exact business definitions depend on the
    source data.
-   A principal recovery percentage is meaningful only when its
    numerator and denominator are clearly defined and aligned to the
    same reporting period.
-   A high-value transaction rule is not equivalent to a fraud-detection
    system.
-   Validate distinct customer counts, retention calculations, and KPI
    denominators before using the figures for formal business reporting.

------------------------------------------------------------------------

## Project Objective

To demonstrate how SQL-based analysis and BI tools can be used to turn
banking loan and transaction data into structured reporting, meaningful
performance indicators, and actionable business insights.

**Tools:** MySQL \| Microsoft Excel \| Power BI \| Tableau
