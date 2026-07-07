📊 ConnectTel Churn Guard: Customer Churn Risk Analytics Dashboard
A dynamic, interactive Power BI dashboard built to identify, segment, and prioritize at-risk telecom customers — enabling data-driven retention strategies before revenue is lost.

2. Short Description / Purpose
The ConnectTel Churn Guard Dashboard is a comprehensive analytics solution designed to help telecom companies understand and reduce customer churn. Built on real telecom data of 7,043 customers, this dashboard moves beyond simple churn reporting — it scores every customer on a 7-factor risk model, segments them into actionable priority tiers, and surfaces the exact behavioral and contractual patterns driving $139.13K in monthly revenue loss.
This tool is intended for use by retention teams, customer success managers, business analysts, and telecom executives who need to identify which customers to target first — and why.

3. Tech Stack
The dashboard was built using the following tools and technologies:

📊 Power BI Desktop — Main data visualization platform used for report creation and interactive dashboard design
📂 Power Query — Data transformation layer used to build the Calendar table, verify data types, and prepare date-based analysis
🧠 DAX (Data Analysis Expressions) — Used for calculated measures (Churn Rate, Revenue At Risk, Avg Tenure), calculated columns (Risk Score, Risk Label, Tenure Bucket), time intelligence (PM/3M/6M/12M/YTD), and dynamic HTML visual generation
🎨 HTML/CSS Visual — Custom SaaS-style risk cards and top customer table rendered natively inside Power BI using HTML Content visual with CONCATENATEX and TOPN
🔢 SQL (MySQL Workbench) — 10 analytical queries written to validate dashboard findings — churn by contract, payment method, tenure, senior citizen, Partner+Dependents combined analysis
📁 File Format — .pbix for development, .csv as data source
📝 Data Modeling — Star schema with fact table (Telco_Churn), Calendar table, Time Period table, and Field Parameter tables for dynamic visual switching


The dataset contains information on 7,043 telecom customers across 23 columns, including:

Customer Profile — gender, senior citizen status, partner, dependents
Services — phone service, internet service (Fiber/DSL/None), tech support, streaming TV/movies, online security/backup
Account Info — tenure (months), contract type, payment method, monthly charges, total charges
Target Variable — Churn (Yes/No) — whether the customer left the company


5. Features / Highlights

🔴 Business Problem
A telecom company was experiencing significant customer attrition — 26.54% of its 7,043 customers had churned, resulting in $139.13K in monthly revenue loss.
The core business challenges were:

No visibility into which customers were about to leave
No understanding of what was driving churn — contract type? Payment method? Service quality?
Wasted retention budget — spending equally on all customers instead of focusing on the highest-risk ones
Reactive approach — only realizing a customer was gone after they left, with no early warning system

Key questions the business needed answered:

Which customers are most likely to leave next month?
What factors are driving churn the most?
How much revenue is at risk right now?
Who should the retention team call first?

🎯 Goal of the Dashboard
To deliver an interactive, self-serve analytics tool that:

Scores every customer on a 7-factor risk model and assigns them to a priority tier (Critical/High/Medium/Low)
Quantifies revenue at risk so the business knows exactly how much money is in danger
Identifies root causes of churn across contract type, payment method, internet service, tenure, and demographics
Provides an actionable customer list — retention teams can filter by risk tier and directly identify who to contact
Tracks trends over time — 12M/6M/3M/PM/YTD time intelligence for period-over-period comparisons


📊 Walkthrough of Key Visuals
Key KPIs (Top Cards)

Total Customers: 7,043
Churned Customers: 2K (1,869)
Churn Rate: 26.54%
Monthly Revenue Lost: $139.13K
Avg Charge Critical: $74.20

Churn Rate by Month (Bar Chart)

Displays monthly churn rate trend across 12 months
Peak: August 30.69% | Low: December 22.24%
Dynamic KPI switching — same chart shows Churn Rate, Retention Rate, Revenue Lost, or Revenue At Risk using Field Parameter

Total Customers by Churn (Donut Chart)

Visual split — 73.46% retained (5K) vs 26.54% churned (2K)

Churn Rate by Contract/Payment/Internet/Tenure (Bar Charts)

Single dynamic chart powered by Field Parameter (Dim_Parameter2)
Switches between 5 dimensions — Contract, InternetService, PaymentMethod, TechSupport, Tenure Bucket
Key finding: Month-to-month = 42.71% vs Two year = 2.83% (15x gap)

Demographic Breakdown (Donut Chart)

Field Parameter switches between Partner, Dependents, Gender, SeniorCitizen
Shows churn rate split for each demographic group

Churn Rate by Partner and Dependents (Matrix Visual)

2-dimensional cross-tab — Partner (rows) × Dependents (columns)
Reveals hidden pattern: No Partner + No Dependents = 34.24% vs both present = 14.24% (2.4x gap)

Customer Priority List (Page 2 — HTML Cards)

4 custom SaaS-style cards for Critical/High/Medium/Low tiers
Each card shows: customer count, monthly revenue, avg charge, fiber%, e-check%, avg tenure with progress bar
Built using DAX HTML measure with CONCATENATEX and CSS styling

Filterable Customer Table

Shows 951 active customers
Filterable by Risk Label, InternetService, Contract, PaymentMethod
Enables retention teams to pull targeted outreach lists directly

Top High-Risk Customers Table (HTML Visual)

Shows top 5 Critical active customers on month-to-month contracts
Sorted by monthly charges descending
Built using TOPN and SELECTCOLUMNS in DAX


💡 Business Impact & Insights
1. $139.13K Monthly Revenue at Risk
Churn rate of 26.54% translates to a quantified monthly revenue loss — giving leadership a concrete number to act on rather than a vague "customers are leaving" problem.
2. Contract Type is the #1 Churn Driver (15x Gap)
Month-to-month customers churn at 42.71% vs 2.83% for two-year customers — a 15x difference. This directly supports a business case for contract migration incentives — offering discounts to move monthly customers to annual plans.
3. Payment Method as a Risk Signal (3x Gap)
Electronic check users churn at 45.29% vs 15.24% for credit card users. Since e-check is manual and non-automatic, these customers are less committed. Migrating them to auto-pay could significantly reduce churn.
4. First Year is the Most Critical Window (5x Gap)
Critical risk customers leave in an average of 11.1 months vs 48.5 months for Low risk customers — nearly 5x faster. This proves the first 12 months of a customer relationship is the highest-risk window, supporting investment in new customer onboarding programs.
5. Isolated Customers are the Most Vulnerable (2.4x Gap)
Customers with neither a partner nor dependents churn at 34.24% vs 14.24% for those with both — a pattern invisible in single-dimension analysis. Family-anchored customers are significantly more stable, suggesting targeted loyalty programs for single/isolated customers.
6. Leading Indicator Discovery
Revenue At Risk continued rising ($9.0K → $9.6K) even as churn rate fell 22% in Q4 — revealing that reported churn improvement masked a growing pool of at-risk active customers. This demonstrates the value of tracking multiple KPIs simultaneously rather than relying on a single metric.

6. Screenshots
(https://github.com/mrpriyesh01/Customer-Churn-Risk-Analysis-/blob/main/dashboard.png)
Page 1 — Main Dashboard:

KPI cards, Churn by Month, Contract/Payment charts, Demographic breakdown

Page 2 — Customer Priority List:

Risk tier cards, filterable customer table, top high-risk customers





