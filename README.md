# 📊 Churn Analysis & Customer Intelligence

> **End-to-End Customer Churn & Revenue Intelligence Analytics Project**

An end-to-end **Customer Churn Analytics** project built for an OTT subscription business to identify high-risk customers, understand churn behavior, quantify revenue impact, and develop actionable retention strategies.

The project integrates **SQL and Python** to analyze customer demographics, subscription information, and customer-support interactions across multiple relational tables.

---

## 🚀 Project Overview

Customer retention is one of the most important challenges in subscription-based businesses.

This project answers three fundamental business questions:

* **Who** is churning or at high risk of churn?
* **Why** are customers leaving?
* **When** does customer churn become most likely?

The analysis combines customer, subscription, and support data to identify churn patterns and translate them into actionable business recommendations.

---

## 🎯 Business Objective

The primary objective is to:

1. Calculate overall customer churn and retention.
2. Identify high-risk customer segments.
3. Analyze churn across subscription plans and contract types.
4. Measure revenue and CLTV impact caused by churn.
5. Investigate the relationship between support escalations and churn.
6. Identify geographical and temporal churn patterns.
7. Recommend data-driven retention strategies.

---

## 🛠️ Tech Stack

### Programming & Analytics

* Python
* NumPy
* Pandas
* SQLite3

### Data Visualization

* Matplotlib
* Seaborn

### Data Analysis

* SQL
* Exploratory Data Analysis
* Feature Engineering
* Aggregation
* GroupBy
* Pivot Tables
* KPI Analysis

The project roadmap specifically uses SQL database extraction through Python, followed by cleaning, feature engineering, analysis, visualization, and executive reporting.

---

## 🗄️ Database Structure

The project works with three primary relational tables:

### `db_customer`

Contains customer-level information:

* `customerid`
* `name`
* `country`
* `state`
* `gender`
* `dob`
* `interests`
* `pincode`

### `db_subscription`

Contains subscription and financial information:

* `customerid`
* `subscription_start_date`
* `subscription_type`
* `renewal_date`
* `plan_type`
* `contract_type`
* `cancellation_date`
* `cancellation_reason`
* `monthly_charges`
* `cltv`
* `churn_score`

### `db_support`

Contains customer-support information:

* `customerid`
* `complaint_date`
* `escalations`
* `csat_score`
* `comment`

These tables enable cross-functional analysis between customer behavior, subscription characteristics, revenue, and support interactions.

---

## 🔄 Analytics Workflow

```text
SQL Database
     ↓
Data Extraction
     ↓
Python + Pandas
     ↓
Data Cleaning
     ↓
Feature Engineering
     ↓
Exploratory Data Analysis
     ↓
KPI Calculation
     ↓
Visualization
     ↓
Business Insights
     ↓
Retention Strategy
```

---

## 📈 Key KPIs

The project calculates more than 20 analytical KPIs.

| KPI                | Description                                        |
| ------------------ | -------------------------------------------------- |
| Churn Rate         | Churned Customers / Total Customers                |
| Retention Rate     | 1 − Churn Rate                                     |
| Churn by Plan      | Churn rate across Basic, Standard & Premium        |
| Churn by State     | Geographic churn analysis                          |
| ARPU               | Revenue generated per active customer              |
| Average Tenure     | Average customer subscription duration             |
| Revenue at Risk    | Revenue associated with high-risk customers        |
| Escalation Rate    | Support escalation frequency                       |
| Avg. Complaints    | Average complaints per customer                    |
| Escalation → Churn | Relationship between support escalations and churn |

The KPI definitions and formulas are documented in the project report.

---

## 🔎 Key Findings

### Overall Churn

**Churn Rate: 28.6%**

**Retention Rate: 71.4%**

This indicates that more than one-quarter of the analyzed customer base has churned.

### Contract Type

A major churn disparity exists between monthly and annual subscribers:

| Contract | Churn Rate |
| -------- | ---------: |
| Monthly  |  **55.6%** |
| Annual   |   **8.3%** |

Monthly subscribers therefore represent a significantly higher-risk segment.

### Revenue Impact

The analysis identified:

* **₹/$73.94 monthly recurring revenue leakage**
* **2,047 CLTV erosion**
* **18% revenue loss**
* Significant revenue exposure among high-risk customers

The report specifically attributes the quantified MRR leakage and CLTV erosion to six at-risk customers.

### Geographic Pattern

**Karnataka** emerged as the most affected state in the analyzed dataset.

### Time Pattern

The highest concentration of churn occurred in **September 2024**.

### Subscription Plan

The largest volume of churn came from the **Basic subscription plan**, although the project notes that this does not necessarily represent the largest revenue impact.

---

## 🧠 Risk Segmentation

A multi-dimensional churn-risk approach was developed using:

* Subscription tenure
* Plan type
* Contract structure
* Support escalations
* Customer churn score
* Customer lifetime value

Customers are segmented into different risk tiers so that retention efforts can focus on customers with the greatest potential business impact.

---

## 💡 Business Recommendations

### 1. Target Monthly Subscribers

Monthly subscribers show substantially higher churn than annual subscribers.

A key strategy is therefore to encourage:

```text
Monthly Plan
     ↓
Targeted Retention Offer
     ↓
Annual Plan Migration
     ↓
Higher Customer Lifetime Value
     ↓
Lower Churn Risk
```

### 2. Investigate Karnataka

The unusually high churn concentration in Karnataka should be investigated for:

* Pricing changes
* Customer complaints
* Technical issues
* Service quality
* Competitor activity

### 3. Investigate September 2024

The September churn spike should be analyzed alongside:

* Pricing changes
* Product changes
* Technical incidents
* Content changes
* Competitor activity
* Customer-support escalations

### 4. Prioritize High-Risk Customers

Customers categorized as **High** and **Medium** risk should be prioritized according to their LTV.

Potential retention channels include:

* Email
* SMS
* Phone outreach
* Personalized offers
* Support intervention

### 5. Analyze Support-Churn Relationship

Support escalations were analyzed alongside churn to identify customers experiencing service-related friction.

The project also decomposes cancellation drivers into areas such as:

* Competitor switching
* Pricing sensitivity
* Content dissatisfaction

---

## 📊 Business Impact

The project transforms raw relational customer data into business-level intelligence.

### From Data

```text
Customer Data
Subscription Data
Support Data
```

### To Intelligence

```text
Churn Patterns
      ↓
Risk Segmentation
      ↓
Revenue at Risk
      ↓
Customer Lifetime Value
      ↓
Retention Strategy
```

This makes the project applicable beyond OTT platforms, including:

* SaaS
* E-commerce
* FinTech
* AdTech
* Telecom
* Subscription businesses

The original project was designed specifically as a portfolio-ready business analytics solution applicable across these industries.

---

## 📂 Suggested Repository Structure

```text
Churn-Analysis-Customer-Intelligence/
│
├── data/
│   ├── customer.csv
│   ├── subscription.csv
│   └── support.csv
│
├── sql/
│   ├── database_schema.sql
│   ├── data_extraction.sql
│   └── churn_analysis.sql
│
├── notebooks/
│   └── churn_analysis.ipynb
│
├── src/
│   ├── data_cleaning.py
│   ├── feature_engineering.py
│   └── analysis.py
│
├── visualizations/
│   ├── churn_by_plan.png
│   ├── churn_by_contract.png
│   └── churn_by_state.png
│
├── reports/
│   └── churn_analysis_report.pdf
│
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/Churn-Analysis-Customer-Intelligence.git
```

Navigate to the project:

```bash
cd Churn-Analysis-Customer-Intelligence
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
notebooks/churn_analysis.ipynb
```

Execute the notebook sequentially to reproduce the analysis.

---

## 📦 Requirements

```text
numpy
pandas
matplotlib
seaborn
jupyter
```

SQLite is used for relational database operations through Python's `sqlite3` module.

---

## 📌 Portfolio Highlights

This project demonstrates practical experience in:

* SQL database integration
* Python data analytics
* Data cleaning
* Feature engineering
* Exploratory data analysis
* Customer segmentation
* Churn analysis
* Revenue analysis
* CLTV analysis
* KPI development
* Data visualization
* Business intelligence
* Data-driven decision making

---

## 📊 Project Outcome

The final analysis identified a **28.6% overall churn rate** and a major difference between monthly and annual subscribers, with monthly subscribers showing **55.6% churn compared with 8.3% for annual subscribers**.

These findings support a targeted **contract-migration and retention strategy**, focusing resources on high-risk customers with significant lifetime value.

---

## 🔮 Future Improvements

Potential extensions include:

* Machine-learning-based churn prediction
* XGBoost / Random Forest risk modeling
* Automated customer risk scoring
* Customer lifetime value prediction
* Real-time churn monitoring dashboard
* Power BI executive dashboard
* Automated retention recommendation engine
* A/B testing of retention campaigns

---

## 👨‍💻 Author

**Mohd Ahmed**

**Data Scientist & Data Analyst**

B.Tech Computer Science & Engineering
New Delhi, India

---

## ⭐ Project Summary

> **An end-to-end customer churn analytics solution that integrates SQL, Python, customer behavior, subscription data, and support intelligence to identify churn risk, quantify revenue exposure, and develop data-driven customer retention strategies.**

---

### 📄 Project Report

The detailed project report contains the complete business challenge, database design, KPI definitions, findings, recommendations, and portfolio summary.

---

**If you found this project useful, consider ⭐ starring the repository.**

**Keep learning. Keep growing.**

