Automobile Sales | RFM Customer Segmentation & Analytics

Project Overview

This project focuses on analyzing automobile sales transactions to understand customer purchasing behavior, identify high-value customers, and uncover customer reactivation opportunities using Recency, Frequency, and Monetary (RFM) Analysis.

The analysis combines Python-based data preparation, exploratory data analysis (EDA), statistical correlation analysis, customer segmentation, and an interactive Power BI dashboard to generate actionable business insights.

Business Objectives

The main objective is to improve customer relationship management and support sustainable revenue growth through data-driven customer segmentation.

Key Business Questions:

Which customer segments contribute the most to total revenue?

How do purchasing behaviors differ across customer segments based on Recency, Frequency, and Monetary?

Which customers should be prioritized for retention, development, and reactivation strategies?

Tools & Technologies

Python: Pandas, NumPy, Matplotlib, Seaborn

Jupyter Notebook: Data cleaning, EDA, and statistical analysis

Power BI: Interactive dashboard and customer segmentation visualization

DAX & Power Query: Data modeling, calculated measures, and data transformation

CSV: Data processing and export

Dataset Overview

The original Automobile Sales dataset contains historical transaction records from January 2018 to May 2020.

Metric

Value

Original Records

2,747

Original Features

20

Unique Orders (Original)

298

Unique Customers

89

Cleaned Transaction Records

2,541

Shipped Orders

277

Total Revenue (Shipped)

9,019,093.90

The dataset includes transaction information, product categories, customer identities, order dates, geographical information, and sales values.

Only transactions with Shipped status were included in the main RFM analysis.

Project Workflow

1. Data Cleaning & Preparation

Data quality assessment was performed before conducting customer analytics.

Activities included:

Data structure and data type validation

Missing value and duplicate detection

Date formatting and transaction consistency checks

Numerical distribution analysis using histograms and boxplots

Outlier detection using the Interquartile Range (IQR) method

Filtering shipped transactions

Customer-level feature engineering

Outliers were retained because unusually high transaction values could represent legitimate high-value purchases.

Result: The cleaned dataset contains 2,541 transaction records representing 277 unique orders and 89 customers.

2. Exploratory Data Analysis (EDA)

EDA was conducted using three analytical approaches.

Univariate Analysis

Examined the distributions of Order Value, Customer Revenue, Purchase Frequency, and Recency.

Key findings:

Order Value distribution was approximately symmetric (skewness = 0.01).

Customer Revenue was strongly right-skewed (skewness = 5.16).

Purchase Frequency was strongly right-skewed (skewness = 5.94).

Approximately 83.15% of customers made 2–3 purchases.

Bivariate Analysis

Investigated relationships between customer purchasing frequency, historical revenue, and recency.

Multivariate Analysis

Used Spearman correlation analysis to evaluate customer purchasing behavior across five variables:

Recency

Frequency

Total Revenue

Average Order Value (AOV)

Product Diversity

Selected correlations:

Relationship

Spearman Correlation

AOV vs Total Revenue

0.71

Frequency vs Total Revenue

0.64

Recency vs Frequency

-0.67

Recency vs Total Revenue

-0.38

Frequency vs AOV

-0.01

Frequency and AOV were nearly uncorrelated, indicating that customers who purchase more frequently do not necessarily have higher average transaction values.

Total Revenue is mathematically related to Frequency and AOV, so these correlations should not be interpreted as causal effects.

3. RFM Customer Segmentation

Customers were evaluated based on three behavioral metrics:

Metric

Definition

Recency

Days since the customer's last purchase

Frequency

Number of unique orders per customer

Monetary

Total historical revenue generated per customer

Each customer received an RFM component score from 1 to 5 based on percentile ranking, with higher scores representing more favorable customer behavior.

The three component scores were summed to produce a combined RFM Score.

Customer Segmentation Rules

Segment

RFM Score

Customers

High Value

12–15

29

Potential

9–11

24

Needs Attention

3–8

36

Segmentation thresholds were defined using a rule-based analytical approach rather than statistical optimization.

4. Power BI Dashboard

An interactive single-page Power BI dashboard was developed to visualize business performance, RFM segmentation, and customer reactivation opportunities.

Dashboard Features

Total Revenue, Total Customers, and Total Orders

Reactivation Candidates KPI

Monthly Revenue Trend

Customer Distribution by Segment

Revenue Contribution by Segment

Customer Share vs Revenue Share

Segment Performance Metrics

Frequency vs AOV Bubble Chart

Top Reactivation Candidates

Interactive Segment, Country, and Product Line Filters

The dashboard enables users to compare customer behavior and revenue contribution across different segments.

Key Findings

1. High-Value Customers Drive the Majority of Revenue

The High Value segment represents 32.58% of customers but contributes 53.21% of total revenue.

This highlights the importance of maintaining relationships with customers who generate substantial historical revenue.

2. Customer Purchasing Behavior Varies Significantly

High Value customers have higher average purchase frequency and monetary value, while customers in the Needs Attention segment have longer recency periods and lower purchase frequency.

Frequency and AOV show almost no monotonic correlation (r = -0.01), suggesting that customer development strategies should address both purchase frequency and transaction value.

3. Customer Reactivation Opportunities Exist

A total of 23 customers (25.84%) were identified as reactivation candidates based on relatively high Recency.

These customers previously generated approximately 1.61 million in historical revenue, representing 17.89% of total revenue.

Potential reactivation targets include Saveley & Henriot, Co., Vida Sport, Ltd., and Herkku Gifts.

These figures represent historical customer value, not guaranteed recoverable revenue.

Strategic Business Recommendations

Customer Segment

Recommended Strategy

High Value

Strengthen retention through loyalty programs, personalized services, and priority customer engagement

Potential

Encourage repeat purchases through upselling, cross-selling, and targeted campaigns

Needs Attention

Evaluate selective reactivation campaigns, prioritizing customers with significant historical revenue

Customer segmentation can help businesses allocate retention and engagement resources more effectively according to customer value and purchasing behavior.

Project Outcome

The analysis demonstrates that customer revenue is unevenly distributed across segments, with High Value customers contributing more than half of total revenue.

Meanwhile, differences in purchasing frequency, average order value, and recency highlight the importance of applying differentiated customer management strategies.

By combining Python-based EDA, RFM segmentation, and Power BI visualization, this project provides a structured analytical framework for identifying valuable customers, supporting retention initiatives, and prioritizing customer reactivation opportunities.

Limitations

RFM segments are based on historical transaction data and predefined scoring thresholds.

High Recency is used as a proxy for inactivity and does not confirm customer churn.

Historical revenue does not represent predicted Customer Lifetime Value (CLV).

Customer-level RFM scores are calculated across the full historical dataset and do not automatically update when dashboard filters are applied.

Recommended strategies have not been experimentally tested for effectiveness.

Conclusion

RFM Customer Segmentation enables businesses to understand customer value, differentiate purchasing behaviors, and prioritize retention and reactivation strategies.

This project demonstrates an end-to-end customer analytics workflow, transforming raw transaction data into actionable business insights using Python and Power BI.
