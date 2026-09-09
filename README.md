Customer Behavior Insight Dashboard

Analysis of customer churn, purchase frequency, and retention behavior using SQL and Python, visualized in an interactive Power BI dashboard — Data Analytics Bootcamp (Sprint 2).

Business Problem
The business relies on repeat purchases, but has no clear view of which customer segments are at highest risk of churn or how long it typically takes before a customer goes inactive.
Without this visibility, retention efforts and marketing spend cannot be targeted effectively — the business ends up treating all customers the same, when risk actually varies sharply by segment.
Hypothesis
Customer segment (High Activity, Mid Activity, Low Activity, Power User) is associated with different churn rates.
Retention drops off in the months immediately following a customer's first purchase, and the drop-off rate differs by segment.
Data & Tools
Tools: SQL (JOIN, Subquery, CTE), Python (pandas, seaborn, matplotlib), Power BI
Data: ~2,220 customers and their order-line history, including first/last order date, recency, tenure, discount sensitivity, and region
Data preparation: Data quality checks and cleaning performed on SQL extracts; customer-level and order-level tables modeled using a Star Schema before analysis
Approach
Defined churn using purchase-recency thresholds (percentile-based: customers with 80+ days between purchases flagged as churned) and calculated a churn rate per customer
Built a cohort retention analysis in Python — grouped customers by their first-purchase month and tracked what % of each cohort was still active in each following month
Segmented customers (High Activity, Mid Activity, Low Activity, Power User) and compared churn and retention patterns across segments and regions
Visualized churn drivers (purchase frequency, average order value) and retention curves using seaborn heatmaps and line charts
Brought the key metrics into an interactive Power BI dashboard for stakeholder-facing reporting
Key Insight
Churn risk varies sharply by segment: early-churn rate is 82.9% for Low Activity customers vs. only 9.5% for Power Users — an ~8x gap, showing that "customer" is too broad a category to target retention efforts effectively.
Retention concentrates the risk early: by month 1 after first purchase, Power User retention is already 43.6% vs. just 5.2% for Low Activity — most of the churn risk materializes almost immediately rather than gradually.
Purchase frequency matters more than spend: churn rate correlates more closely with how often a customer buys than with their average order value, suggesting frequency-based triggers (e.g., a follow-up nudge after a customer's typical purchase window passes) would be a more effective retention lever than discount-based offers alone.
Dashboard
<!-- Add dashboard screenshot here, e.g. ![Dashboard](dashboard.png) -->
Links
Notebook (churn & cohort retention analysis) <!-- add exported .ipynb link once uploaded to the repo -->
