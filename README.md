# Lending Club Loan Default Analysis

## Executive Summary

Loan default is an important risk factor for lending institutions because it can affect portfolio performance and financial sustainability. Understanding borrower and loan characteristics associated with default can help identify patterns in credit risk.

This project analyzes the **Lending Club loan dataset** to examine borrower characteristics, loan characteristics, and factors associated with loan default. The analysis combines **Python for data cleaning and exploratory data analysis (EDA)** with **Power BI for analytical reporting and visualization**.

Loan outcomes were classified as **Defaulted**, **Did Not Default**, or **Outcome Unknown**. Only loans with known outcomes were retained for the Power BI analysis, ensuring that default-rate calculations were based on finalized loans.


## Business Problem

The analysis aims to answer questions such as:

- What proportion of finalized loans were defaulted?
- How does default rate vary across borrower characteristics?
- How does DTI relate to default risk?
- How do interest rate, loan amount, term, grade, and purpose relate to default?
- How has loan performance changed over time?


## Project Objectives

The project was designed to:

- Assess the overall default rate within the finalized loan portfolio.
- Analyze borrower characteristics associated with loan default.
- Examine how credit characteristics such as DTI, delinquencies, and credit history relate to default risk.
- Evaluate how loan characteristics such as loan amount, interest rate, term, grade, and purpose relate to default.
- Compare default rates across different borrower and loan segments.
- Analyze changes in loan volume, loan amounts, interest rates, and default rates over time.
- Provide an interactive dashboard for exploring loan portfolio and default risk patterns.

---

## Data & Methodology

The project followed a structured workflow:

```text
Lending Club Dataset
        ↓
Data Cleaning & Preparation
        ↓
Exploratory Data Analysis
        ↓
Loan Outcome Classification
        ↓
Filter to Known Outcomes
        ↓
Power BI Analysis
        ↓
Interactive Dashboard ```text
### Data Cleaning & EDA

Python and Pandas were used to:

- Inspect the dataset structure and data types.
- Assess missing values and data quality.
- Remove unnecessary columns.
- Review unusual and extreme values.
- Explore borrower, credit, and loan characteristics.

### Loan Outcome Classification

Loan statuses were grouped into three categories:

#### Defaulted

- Charged Off
- Default
- Does not meet credit policy — Charged Off

#### Did Not Default

- Fully Paid
- Does not meet credit policy — Fully Paid

#### Outcome Unknown

- Current
- In Grace Period
- Late loans and other unresolved outcomes

Loans with unknown outcomes were excluded from the finalized dataset used in Power BI.

### Power BI Analysis

The finalized dataset was imported into Power BI, where **DAX measures and calculated columns** were used to analyze:

- Default rate
- Loan volume
- Loan amounts
- Average loan amount
- Average interest rate
- Defaulted loan amounts
- Borrower and loan segments

Income, DTI, and loan amount were grouped into bands to make comparisons easier.


## Dashboard

The Power BI dashboard contains three main analytical areas:

### 1. Portfolio Overview

Provides an executive-level view of:

- Total loans
- Total loan amount
- Total defaulted loans
- Default rate
- Average loan amount
- Average interest rate
- Yearly portfolio trends

### 2. Borrower Risk Analysis

Examines default rates across borrower and credit characteristics, including:

- Annual income
- Employment length
- DTI
- Home ownership
- Verification status
- Credit characteristics

### 3. Loan Characteristics & Default

Analyzes default rates across:

- Loan amount
- Interest rate
- Loan term
- Grade
- Sub-grade
- Loan purpose

## Default Rate

Default rate was calculated using only loans with known final outcomes:

```text
Default Rate =
Defaulted Loans
──────────────────────────── × 100
Defaulted + Did Not Default Loans

This prevents active or unresolved loans from being incorrectly treated as non-defaulted loans.

---

## Key Insights

The dashboard highlights several notable patterns in the finalized loan portfolio:

- **DTI shows a clear variation in default rates.** Default rates increase from about **15% for borrowers with DTI below 10%** to approximately **34% for borrowers with DTI between 40–50%**, before declining for the highest DTI bands.

- **Lower-income borrowers have higher observed default rates.** The default rate is approximately **25% for borrowers earning under $25K**, compared with about **16% for borrowers earning $100K or more**.

- **Higher loan amounts are associated with progressively higher observed default rates.** Default rates increase from approximately **16% for loans below $5K** to more than **23% for loans of $20K or more**.

- **Loan term shows a substantial difference in default rates.** Loans with a **60-month term have a default rate of about 32%**, compared with approximately **16% for 36-month loans**.

- **Default rates increase substantially across loan grades.** Grade A has the lowest observed default rate at around **4%**, while Grade G approaches **50%**. The pattern shows progressively higher default rates as the loan grade moves from A toward G.

- **Interest rate shows a strong positive association with default rate.** Default rates increase from approximately **8% for loans with interest rates of 5–10%** to nearly **48% for loans above 25%**.

- **Default rates differ across loan purposes.** Small-business loans have the highest observed default rate at around **29%**, while wedding loans have one of the lowest at approximately **12%**.

- **The amount of defaulted loans changed considerably over time.** Defaulted loan amounts increased sharply and reached their highest level around **2015**, before declining through 2018.

- **Employment length shows relatively similar default rates across most categories.** Most employment-length groups are close to **20%**, while loans where employment length was not specified show a noticeably higher rate of approximately **27%**.


## Skills Demonstrated

### Python

- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

### Power BI

- Data modeling
- DAX
- Calculated columns
- Data segmentation
- Interactive dashboards
- Time-based analysis

### Business Analytics

- Data cleaning
- Exploratory data analysis
- Credit risk analysis
- Portfolio analysis
- Data visualization
- Business storytelling


## Conclusion

This project demonstrates how combining **borrower risk analysis and loan characteristics** can provide a clearer understanding of loan default patterns.

The analysis highlights differences in observed default rates across **DTI, income, interest rate, loan amount, term, grade, and loan purpose**, providing insight into areas of higher observed credit risk within the loan portfolio.

From a technical perspective, the project showcases an end-to-end workflow using **Python and Power BI**. Python was used for data cleaning, outcome classification, and EDA, while Power BI was used for **DAX, segmentation, visualization, and interactive reporting**.

Overall, the project demonstrates the ability to transform a large lending dataset into **clear business insights that support portfolio and credit risk analysis**.
