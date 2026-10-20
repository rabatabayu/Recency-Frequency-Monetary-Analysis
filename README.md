Automobile Sales | RFM Customer Segmentation
End-to-end Customer Analytics Project using Python & Power BI

This project analyzes historical automobile sales transactions to understand customer value, purchasing behavior, and reactivation opportunities. It combines data cleaning, exploratory data analysis (EDA), Recency–Frequency–Monetary (RFM) segmentation, and an interactive Power BI dashboard to support customer-focused business decisions.
Business Questions
1. Customer Value: Which customer segment contributes the most revenue?
2. Customer Behavior: How do Recency, Frequency, Monetary, and Average Order Value (AOV) differ across segments?
3. Reactivation: Which previously valuable customers have not purchased recently and may be worth contacting again?
Tools
- Python: Pandas, NumPy, Matplotlib, Seaborn
- Jupyter Notebook: Data cleaning, EDA, and feature engineering
- Power BI: Data modeling, Power Query, DAX, and interactive visualization
Dataset & Preparation
Metric	Result
Original dataset	2,747 rows, 20 columns
Original unique orders	298
Cleaned Shipped records	2,541
Unique shipped orders	277
Unique customers	89
Revenue from shipped orders	9,019,093.90
Analysis period	January 2018 – May 2020


Data preparation included validation of missing values, duplicates, date formats, and transaction consistency. Outliers were examined with boxplots and the Interquartile Range (IQR) and retained when plausible as genuine high-value purchases. The RFM analysis includes only orders with the Shipped status.
Analytical Workflow
1. Exploratory Data Analysis
Univariate: Order Value, Customer Revenue, Purchase Frequency, and Recency distributions.

Bivariate: Relationships among Frequency, Monetary, and Recency, including sensitivity checks for extreme customers.

Multivariate: Spearman correlation heatmap and a customer-level Frequency vs AOV bubble chart.

Selected findings:
Analysis	Finding
Order Value distribution	Approximately symmetric (skewness 0.01)
Customer Revenue distribution	Strong right skew (skewness 5.16)
Purchase Frequency distribution	Strong right skew (skewness 5.94)
Frequency vs Monetary	Spearman 0.64
Recency vs Frequency	Spearman −0.67
Frequency vs AOV	Spearman −0.01


Frequency and AOV were nearly uncorrelated, suggesting different buying patterns across customers. Correlations involving total revenue are partly influenced by the identity Total Revenue = Frequency × AOV and should not be treated as causal evidence.
2. RFM Scoring & Segmentation
Each customer was assigned a 1–5 percentile-based score for each RFM component:
- Recency (R): Days since the last shipped order; lower is better.
- Frequency (F): Number of unique shipped orders; higher is better.
- Monetary (M): Total historical revenue per customer; higher is better.
The three scores were summed and grouped using rule-based thresholds:
Segment	RFM Score	Customers	Customer Share	Revenue Share
High Value	12–15	29	32.58%	53.21%
Potential	9–11	24	26.97%	22.10%
Needs Attention	3–8	36	40.45%	24.69%


These thresholds are analytical assumptions, not statistically optimized segment boundaries.
3. Customer Reactivation Analysis
Customers with Recency ≥ 251 days (the upper quartile of Recency) were flagged as reactivation candidates.
- 23 customers (25.84% of customers) met the criterion.
- Their combined historical revenue was approximately 1.61M, equivalent to 17.89% of overall revenue.
- Examples of priority candidates include Saveley & Henriot, Co., Vida Sport, Ltd., and Herkku Gifts.
This identifies customers who may warrant follow-up; it does not estimate recoverable revenue or confirm churn.
Power BI Dashboard
The one-page interactive dashboard includes:
- KPI cards: Total Revenue, Total Customers, Total Orders, Reactivation Candidates
- Monthly Revenue Trend
- Customer Distribution by Segment
- Revenue Contribution and Customer Share vs Revenue Share
- Segment Performance (average R, F, and M)
- Frequency vs AOV bubble chart
- Top Reactivation Candidates table
- Slicers for Segment, Country, and Product Line
Dashboard screenshot: Add an image of your final Power BI dashboard to the repository and link it here.

Key Business Insights
1. High Value customers are the main revenue contributors. Although they account for only 32.58% of customers, they generate 53.21% of total historical revenue.

2. Customer purchasing patterns differ. Higher purchase frequency does not necessarily imply a larger average order value (Spearman = −0.01), supporting differentiated retention and upselling approaches.

3. Reactivation opportunities exist beyond a single segment. The 23 candidates include both Potential and Needs Attention customers, so outreach should consider individual recency and historical value—not segment labels alone.
Business Recommendations
Segment	Suggested action
High Value	Prioritize retention with personalized service and loyalty initiatives.
Potential	Encourage repeat purchases, cross-selling, and higher basket values.
Needs Attention	Test selective win-back campaigns, prioritizing customers with meaningful historical spending.


Limitations
- Findings describe a historical dataset ending in May 2020, not current customer activity.
- RFM scores reflect the full historical dataset; dashboard category filters do not recalculate customer RFM scores.
- A high Recency value indicates inactivity relative to the dataset's snapshot date, not confirmed churn.
- Revenue is not profit, and historical Monetary is not predictive Customer Lifetime Value (CLV).
- Recommendations are hypotheses to test, not proven intervention outcomes.
Conclusion
RFM analysis turns transaction-level sales data into actionable customer segments. The project identifies customers worth retaining, groups with potential for growth, and historical reactivation candidates—providing a practical framework for customer relationship strategies using Python and Power BI.
