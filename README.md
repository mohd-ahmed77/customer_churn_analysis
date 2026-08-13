# customer_churn_analysis
📊 OTT Subscription Churn Analysis & Retention Strategy

An end-to-end data analytics project focused on understanding subscriber behavior, identifying high-risk churn vectors, and formulating actionable retention strategies for an Over-The-Top (OTT) streaming platform.

👨‍💻 Project Author

Author: Mohd Ahmed

Role: Data Scientist & Analyst

Motto: "Keep learning & keep growing."

📌 Executive Summary

Acquiring new subscribers in a hyper-competitive OTT market is costly. This project analyzes multi-table relational subscriber data to determine who is leaving, why they are cancelling, and when churn risk reaches its peak.

Key Performance Indicators (KPIs)

Metric

Value

Insight

Overall Churn Rate

28.6%

28.6% total subscriber drop-off rate

Retention Rate

71.4%

Strong baseline retention across core user base

Average ARPU

₹18.8k

Average Revenue Per User

Average Tenure

1,451 days

~4 years mean account lifespan

Direct Revenue Loss

₹74k (18.7%)

Lost revenue out of ₹395k total

CLTV Risk Exposure

₹2,047k

Cumulative Customer Lifetime Value lost

🔍 Key Findings & Insights

1. 🚨 Strongest Churn Driver: Contract Type

Monthly Contracts: 55.6% churn rate.

Annual Contracts: 8.3% churn rate.

Impact: Subscribers on monthly plans are 6.7× more likely to churn compared to annual subscribers.

Strategic Priority: Converting 15% of monthly subscribers to annual contracts cuts total churn by approximately 22%.

2. 📍 High Risk Concentrations

Plan Segment: The Basic Plan accounts for the largest volume of churn.

Temporal Spike: A distinct spike in subscriber cancellations occurred in September 2024.

Geographic Focus: Karnataka State exhibited the highest regional concentration of churned accounts.

🛠️ Data Architecture & Pipeline

The project integrates data across three core relational tables:

┌──────────────────┐       ┌──────────────────────┐       ┌──────────────────┐
│   db_customer    │       │   db_subscription    │       │    db_support    │
├──────────────────┤       ├──────────────────────┤       ├──────────────────┤
│ • customerid     │ ──┐   │ • customerid         │   ┌── │ • customerid     │
│ • name           │   └───┼───► • start/renewal  │◄──┘   │ • complaint date │
│ • country/state  │       │ • plan/contract      │       │ • escalations    │
│ • gender/DOB     │       │ • cancellation date  │       │ • CSAT score     │
│ • interests      │       │ • monthly charges/LTV│       │ • comments       │
└──────────────────┘       └──────────────────────┘       └──────────────────┘


End-to-End Analytical Pipeline

Extraction: Querying relational data using SQL (sqlite3).

Data Cleaning: Null handling, data type standardization, and anomaly removal.

Feature Engineering: Creating churn indicators, tenure brackets, and risk scores.

Exploratory Data Analysis (EDA): Aggregations, distribution checks, and cross-tabulations.

Visualization: Plotting trends using Python (seaborn / matplotlib) and HTML reporting.

Actionable Recommendations: Formulating executive-ready business strategies.

🎯 Risk Prioritization Matrix

Priority

Risk Profile

Target Segment

Actionable Strategy

01 - High

High Risk + High LTV

Annual users with support escalations

Immediate personal outreach & dedicated SLA

02 - Medium

Medium Risk + High LTV

Long-tenure users with service drops

Proactive retention offers prior to renewal

03 - Operational

Monthly Plan Exposure

Highly engaged monthly subscribers

Automated annual-plan upgrade discount campaigns

04 - Diagnostic

Basic Plan Churners

Price-sensitive low LTV subscribers

Product feedback surveys & pricing tier adjustments

🚀 Recommended Action Roadmap

Karnataka Deep-Dive Audit: Investigate potential service outages, price increases, or competitor activities in September 2024.

Contract Migration Campaign: Launch targeted annual migration incentives (15–20% discount) for engaged monthly users.

High-LTV Retention Protocol: Deploy proactive outreach to protect top revenue-generating accounts.

Support Ticket Integration: Connect CSAT drops and unresolved support tickets to automated retention triggers.

🧰 Tech Stack

Language: Python 3.x

Data Processing: pandas, numpy

Database: SQL, sqlite3

Data Visualization: seaborn, matplotlib

Presentation & Reporting: HTML5, CSS3, Tailwind CSS, FontAwesome

📂 Repository Structure

├── data/
│   ├── raw/                  # Source CSV/SQL database dumps
│   └── processed/            # Cleaned data ready for analysis
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_eda_churn_analysis.ipynb
│   └── 03_risk_scoring.ipynb
├── reports/
│   └── churn_analysis_presentation.html  # Interactive Executive Presentation
├── scripts/
│   ├── pipeline.py           # Data processing pipeline
│   └── utils.py              # Helper functions
├── README.md                 # Project Documentation
└── requirements.txt          # Python dependencies


💻 How to Run

Clone the Repository:

git clone https://github.com/your-username/ott-churn-analysis.git
cd ott-churn-analysis


Install Dependencies:

pip install -r requirements.txt


Run the Analysis Pipeline:

python scripts/pipeline.py


View Executive Presentation:
Open reports/churn_analysis_presentation.html in any modern web browser.

📜 License

This project is open-source and available under the MIT Licens

<i
