# 🚗 Automobile Sales | RFM Customer Segmentation

### 📊 End-to-End Customer Analytics Project | Python & Power BI

## 📌 Project Overview

This project analyzes automobile sales data to understand customer purchasing behavior, identify high-value customers, and uncover reactivation opportunities using **Recency, Frequency, and Monetary (RFM) Analysis**.

The project covers an end-to-end data analytics workflow, from data cleaning and exploratory data analysis (EDA) to RFM customer segmentation, interactive dashboard development, and strategic business recommendations.

---

## 🎯 Business Objectives

**Problem Statement**

How can RFM-based customer segmentation help automobile businesses identify valuable customers, improve customer retention, and prioritize reactivation opportunities?

**Key Business Questions**

1. Which customer segments contribute the most to total revenue?
2. How do purchasing behaviors differ across customer segments based on Recency, Frequency, and Monetary?
3. Which customers should be prioritized for retention and reactivation strategies?

---

## 🛠️ Tools & Technologies

| Tools | Purpose |
|---|---|
| 🐍 Python | Data Cleaning, EDA, Statistical Analysis |
| 📚 Pandas & NumPy | Data Manipulation & Feature Engineering |
| 📈 Matplotlib & Seaborn | Statistical Visualization |
| 📊 Power BI | Interactive Dashboard |
| 🔧 DAX & Power Query | Data Modeling & KPI Development |
| 📓 Jupyter Notebook | Data Analysis & Documentation |

---

## 📂 Dataset Overview

The dataset contains historical automobile sales transactions from **January 2018 to May 2020**.

| Description | Value |
|---|---:|
| Original Records | 2,747 |
| Original Features | 20 |
| Unique Customers | 89 |
| Unique Orders | 298 |
| Cleaned Transactions | 2,541 |
| Completed Shipped Orders | 277 |
| Total Shipped Revenue | 9.02M |

Only **Shipped** transactions were selected for the main customer analysis.

---

## 🔍 Analytical Workflow

### 1️⃣ Data Cleaning & Preparation

- Checked missing values, duplicates, and data types.
- Converted transaction dates into datetime format.
- Identified outliers using boxplots and the Interquartile Range (IQR) method.
- Retained legitimate outliers to preserve high-value customer information.
- Filtered shipped transactions and performed customer-level feature engineering.

### 2️⃣ Exploratory Data Analysis (EDA)

Performed univariate, bivariate, and multivariate analyses to identify customer purchasing patterns.

**Key EDA Findings:**

- Order Value distribution was approximately symmetric (skewness = 0.01).
- Customer Revenue was strongly right-skewed (skewness = 5.16).
- Purchase Frequency was strongly right-skewed (skewness = 5.94).
- Frequency and Monetary showed a positive Spearman correlation (r = 0.64).
- Recency and Frequency showed a negative Spearman correlation (r = -0.67).
- Frequency and AOV were nearly uncorrelated (r = -0.01).

These findings suggested that customers have different purchasing behaviors, supporting the need for customer segmentation.

### 3️⃣ RFM Customer Segmentation

Customers were scored from 1 to 5 based on:

- **Recency (R):** Days since the last purchase.
- **Frequency (F):** Number of unique transactions.
- **Monetary (M):** Total historical customer revenue.

Customers were then grouped into three segments using rule-based RFM scores.

| Customer Segment | RFM Score | Customers | Customer Share |
|---|---|---:|---:|
| 🟢 High Value | 12–15 | 29 | 32.58% |
| 🔵 Potential | 9–11 | 24 | 26.97% |
| 🟠 Needs Attention | 3–8 | 36 | 40.45% |

### 4️⃣ Power BI Dashboard

Developed an interactive dashboard containing:

- Revenue, Orders, Customers & Reactivation KPIs
- Monthly Revenue Trend
- Customer Distribution by Segment
- Revenue Contribution Analysis
- Customer Share vs Revenue Share
- Segment Performance Analysis
- Frequency vs AOV Bubble Chart
- Top Reactivation Candidates

**Interactive Filters:** Customer Segment, Country, and Product Line.

---

## 💡 Key Business Insights

### 🥇 1. High-Value Customers Drive Revenue

**32.58% of customers generated 53.21% of total revenue.**

The High Value segment contributes the largest revenue share, highlighting its importance for customer retention strategies.

### 📈 2. Purchase Frequency Does Not Always Mean Higher AOV

The Spearman correlation between Frequency and AOV was approximately **-0.01**, indicating almost no monotonic relationship.

This suggests that customers with frequent purchases do not necessarily have higher average transaction values.

### 🔄 3. Customer Reactivation Opportunities

**23 customers (25.84%)** were identified as reactivation candidates using a historical Recency threshold.

These customers contributed **17.89% of total historical revenue**, representing approximately 1.61M in previous sales.

The findings highlight opportunities to prioritize customer reactivation based on historical value and inactivity.

---

## 🚀 Strategic Business Recommendations

| Segment | Recommended Strategy |
|---|---|
| 🟢 High Value | Customer retention, loyalty programs, personalized services |
| 🔵 Potential | Repeat purchase campaigns, upselling, cross-selling |
| 🟠 Needs Attention | Selective reactivation, personalized win-back campaigns |

The proposed strategies focus on improving customer engagement while prioritizing customer groups based on their historical purchasing behavior.

---

## 🏁 Project Outcome

The analysis revealed that **customer revenue is unevenly distributed across segments**, with High Value customers generating more than half of total revenue.

Different combinations of Recency, Frequency, and Monetary demonstrate the importance of applying differentiated customer management strategies.

**By integrating Python-based analytics, RFM segmentation, and Power BI visualization, this project transforms historical transaction data into actionable insights for customer retention, development, and reactivation.**

---

## 📝 Analytical Notes

- RFM segmentation uses predefined rule-based thresholds.
- Recency is measured relative to the historical dataset, not the current date.
- Reactivation candidates represent potential targets, not confirmed churned customers.
- Historical customer revenue does not represent predicted Customer Lifetime Value (CLV).
- Business recommendations are analytical proposals and have not been experimentally validated.

---

### ⭐ Project Focus

**Customer Analytics | RFM Segmentation | Revenue Analysis | Customer Retention | Power BI Dashboard | Python EDA**
