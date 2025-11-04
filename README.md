Petrol Pump ETL & Analytics using Informatica IICS

Overview:
This project focuses on detecting stock discrepancies, automating alerts, and ranking branch performance for multiple petrol pump outlets using Informatica Intelligent Cloud Services (IICS).
By integrating data from multiple sources such as fuel stock, sales, payments, and expenses, the ETL workflows deliver early anomaly detection, profitability insights, and automated reporting — enabling data-driven decision-making in fuel management.

Objectives:
• Detect mismatches between expected vs. actual stock and revenue.
• Automate alerts for low stock, budget deviation, and fraud detection.
• Calculate and track daily net profit and branch-level performance.
• Enable intelligent reordering of lubricants based on consumption trends.
• Provide business intelligence dashboards for management decisions.

| File Name               | Description                               | Key Columns                                                     |
| ----------------------- | ----------------------------------------- | --------------------------------------------------------------- |
| Branches.csv            | Details of petrol pump branches           | Branch_ID, Branch_Name, Location                                |
| Fuel_Stock.csv          | Daily fuel stock data                     | Stock_ID, Branch_ID, Fuel_Type, Quantity, Stock_Date            |
| Daily_Sales_Report.csv  | Fuel sales records                        | Sale_ID, Branch_ID, Fuel_Type, Quantity_Sold, Total_Sale_Amount |
| Expenditure.csv         | Branch-level expenses                     | Expenditure_ID, Branch_ID, Expense_Type, Amount                 |
| Lubricants.csv          | Lubricant details and cost                | Lubricant_ID, Lubricant_Name, Unit_Cost                         |
| Branch_Lubricants.csv   | Mapping of lubricants stocked in branches | Branch_ID, Lubricant_ID, Quantity                               |
| Performance_Metrics.csv | Aggregated daily performance metrics      | Metric_ID, Branch_ID, Daily_Sales, Profit                       |
| Stock_Alerts.csv        | Alerts for low stock thresholds           | Alert_ID, Branch_ID, Fuel_Type, Current_Stock                   |

Key ETL Scenarios:

1.Intelligent Lubricant Reordering

Analyzes weekly sales and current stock to trigger lubricant reorder alerts.

Transformations Used: Aggregator, Expression, Filter, Update Strategy.

2.Branch-Level Stock Alert

Calculates stock percentage and flags branches below safe thresholds.

Transformations Used: Expression, Filter, Router.

3.Fuel Wastage Detection

Compares expected vs. recorded closing stock to detect losses or errors.

Transformations Used: Expression, Filter, Sorter.

4.Daily Net-Profit Calculation

Aggregates branch sales and expenses to compute daily profit.

Transformations Used: Aggregator, Expression.

5.Pending Payment Detection

Compares sales and payment collections to detect mismatches.

Transformations Used: Joiner, Expression, Filter, Sorter.

6.Branch Performance Ranking

Calculates revenue per litre and ranks branches accordingly.

Transformations Used: Aggregator, Expression, Rank, Router.

7.Payment Spike Detection

Uses Z-score analysis to identify abnormal payment spikes or anomalies.

Transformations Used: Normalize, Aggregator, Expression, Filter.

8.Budget Deviation Alerts

Flags expenditure exceeding ₹40,000 to trigger financial alerts.

Transformations Used: Expression, Target.

9.Lubricant Inventory Upsert

Automates insert/update of lubricant data ensuring inventory accuracy.

Transformations Used: Joiner, Router, Update Strategy.

10.Branch-wise Stock Summary

Aggregates fuel and lubricant data to generate consolidated stock reports.

Transformations Used: Aggregator, Target.

Business Insights:
• Early detection of fuel theft or leakage.
• Accurate branch-wise profitability tracking.
• Automated budget monitoring and financial alerts.
• Trend-based restocking and inventory optimization.
• Enhanced fraud detection and operational transparency.

Tools and Technologies:
• ETL Platform: Informatica Intelligent Cloud Services (IICS)
• Database: MySQL / CSV Files
• Documentation: ER Diagrams, Data Dictionary, Flow Diagrams

Author:
Pragatilaxmi Itigowni
B.E. in Artificial Intelligence Engineering
KLE Technological University, Hubballi
Email: pariitigowni@email.com
