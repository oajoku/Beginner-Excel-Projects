Overview
--------------------------------------------------------------------------------------------------------------------------------------------
This project demonstrates how to build a dynamic Financial Forecasting Dashboard using Microsoft Excel, focusing on:

--------------------------------------------------------------------------------------------------------------------------------------------

Revenue and expense forecasting for businesses.



Interactive What-If Analysis to evaluate scenarios (e.g., best-case and worst-case).


Basic macros for automation.


Advanced data visualization for stakeholder-ready presentations.


The project showcases how to create a user-friendly and professional tool for financial decision-making without requiring advanced VBA programming.



Features

--------------------------------------------------------------------------------------------------------------------------------------------
What-If Analysis:



Used to project future cash flows under varying assumptions (e.g., sales growth rates, expense fluctuations).


Includes dynamic scenarios like best-case and worst-case projections.


Scenario Manager:
--------------------------------------------------------------------------------------------------------------------------------------------
Showcases the impact of different assumptions on overall financial performance.


Easy switching between scenarios for comparative analysis.


Basic Macros:

Automates repetitive tasks like refreshing data and running What-If Analysis.


Simplifies the user experience with recorded macros.


Interactive Dashboard:

Tracks total revenue, profit, profit margins, and projected expenses.


Includes visually appealing charts, trend arrows, and KPIs for quick insights.


Dynamic Updates:

Automatically recalculates and adjusts when new inputs are added.


Ensures accuracy and saves time.


Skills Demonstrated


Financial data preparation and analysis.


Advanced Excel functions: PMT, IPMT, and SUM.


What-If Analysis and Scenario Manager for financial projections.


Basic macros for automation and efficiency.


Project Goal


The goal was to build a financial forecasting model for McDonald’s to:



Track and analyze key financial metrics like revenue, profit, and margins.


Create interactive tools to visualize trends and assist in decision-making.


Improve efficiency and accuracy in forecasting without advanced programming.

--------------------------------------------------------------------------------------------------------------------------------------------
Dataset
The dataset used in this project includes:

Monthly revenue, estimated expenses, and profit information.


Expenses were calculated as 70% of revenue, based on industry standards.


Key performance indicators (KPIs) like total revenue, profit, and profit margins were derived from the data.


Source: A hypothetical dataset based on financial datasets from Kaggle.
--------------------------------------------------------------------------------------------------------------------------------------------
Process


Step 1: Data Analysis and Preparation


Data Challenges:


The dataset lacked explicit expense data, making profit calculations difficult.


Solution: Estimated expenses as 70% of revenue using the formula:


Copy code


=Revenue * 0.7  


KPI Calculation:


Total Revenue: =SUM(range)


Total Profit: Revenue - Expenses


Profit Margin: (Profit / Revenue) * 100


Step 2: Dashboard Creation


Designed a clean, intuitive layout with key KPIs at the top.


Incorporated line charts for trends and column charts for scenario comparisons.


Used dynamic formulas and cell references to ensure real-time updates.


Step 3: Scenario Management


Created best-case and worst-case scenarios using Scenario Manager.


Adjusted assumptions (e.g., sales growth rates) to see their impact.


Resolved referencing issues to ensure accurate results when switching scenarios.

--------------------------------------------------------------------------------------------------------------------------------------------
Challenges and Solutions


Missing Expense Data:

Challenge: The dataset didn’t include expenses.


Solution: Estimated expenses as 70% of revenue based on industry norms.


Dynamic Dashboard Updates:

Challenge: Ensuring charts and KPIs updated in real time.


Solution: Used dynamic formulas and linked references for automatic updates.


Scenario Manager Issues:

Challenge: Scenarios didn’t reflect changes correctly.


Solution: Rebuilt scenarios with clean data and corrected cell references.

--------------------------------------------------------------------------------------------------------------------------------------------


Results


Created a dynamic dashboard showcasing key financial metrics for McDonald’s.


Streamlined forecasting with automated What-If Analysis and Macros.


Produced actionable insights using clean visualizations and real-time updates.

--------------------------------------------------------------------------------------------------------------------------------------------
Portfolio Highlights


Forecasting Accuracy: Integrated dynamic scenarios for reliable projections.


Ease of Use: Simplified data refreshes and analysis with basic macros.


Visualization: Advanced formatting techniques made the dashboard stakeholder-ready.


Practical Skills: Showcased Excel tools for real-world business scenarios.

--------------------------------------------------------------------------------------------------------------------------------------------
Future Enhancements


Incorporate Power BI or Tableau for advanced visualization and interactivity.


Add more complex macros for enhanced automation.


Expand the dataset to include more granular expense details.

--------------------------------------------------------------------------------------------------------------------------------------------


How to Use


Open the Excel file and navigate to the Dashboard tab.


Update inputs like revenue and expense assumptions in the Data tab.


Use the Scenario Manager to switch between best-case and worst-case projections.


Run the macro to refresh data or perform What-If Analysis.

--------------------------------------------------------------------------------------------------------------------------------------------
Safety Note


Ensure macros are from trusted sources.


Keep your antivirus software updated to prevent potential threats.

--------------------------------------------------------------------------------------------------------------------------------------------
Conclusion
This project provided a hands-on opportunity to develop financial forecasting and data visualization skills. It highlighted my ability to solve real-world business challenges dynamically and efficiently.


