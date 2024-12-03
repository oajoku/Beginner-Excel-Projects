Customer Segmentation Analysis for Marketing

--------------------------------------------------------------------------------------------------------------------------------------------
Project Overview
This project involves performing a customer segmentation analysis using a mall customer dataset obtained from Kaggle. The goal of this analysis is to classify customers into meaningful groups based on their demographic and spending patterns. These insights can assist marketing teams in designing tailored strategies for different customer segments, such as VIP loyalty programs or budget-friendly promotions.


--------------------------------------------------------------------------------------------------------------------------------------------
Difficulty Level

Medium
--------------------------------------------------------------------------------------------------------------------------------------------
Dataset Overview

--------------------------------------------------------------------------------------------------------------------------------------------
Details	Description

--------------------------------------------------------------------------------------------------------------------------------------------
Rows	200
Columns	5
Attributes	- CustomerID: 
Unique identifier (integer)
- Genre:
- Gender of customer (Male/Female)
- Age:
- Age of customer (integer)
- Annual Income (k$):
-  Annual income in thousands (integer)
- Spending Score (1-100): Spending behavior score (integer)


--------------------------------------------------------------------------------------------------------------------------------------------
Project Steps

--------------------------------------------------------------------------------------------------------------------------------------------
1. Data Preprocessing


Data Cleaning

Converted Text to Numbers:
Ensured that CustomerID values were recognized as numerical data by Excel.
Removed Duplicates:
Used the Remove Duplicates feature in Excel to eliminate any redundant entries.
Outlier Detection: 
Identified outliers for Age, Annual Income, and Spending Score using the 1.5 × IQR Rule:
Quartile values (Q1, Q3) were calculated using Excel’s =QUARTILE() function.
Outlier boundaries:
Lower: Q1 - (1.5 * IQR)
Upper: Q3 + (1.5 * IQR)
Outliers were flagged using the =IF() function.

Decision: 
Kept the two outliers found in the Annual Income column for analysis.

--------------------------------------------------------------------------------------------------------------------------------------------
Challenges Encountered

--------------------------------------------------------------------------------------------------------------------------------------------
Initial confusion with applying quartile calculations for individual columns.
Resolved by referencing fixed cells for Q1 and Q3 when using the outlier formula across rows.
Learned to lock cell references with $ symbols for formula consistency.


3. Data Transformation
   
Categorization Using Excel's IF Function
Created three new columns to categorize data for age, income, and spending behavior.

Age Categories:

Formula: 
=IF(Age <= 25, "Under 25", IF(Age <= 45, "25-45", "Over 45"))
Categories:

"Under 25": 
Customers aged 25 or below.
"25-45": 
Customers aged 26 to 45.
"Over 45": 
Customers aged above 45.

Income Categories:
Formula: 
=IF(AnnualIncome <= 50, "Low Income", IF(AnnualIncome <= 100, "Medium Income", "High Income"))
Categories:

"Low Income":
Annual income ≤ $50,000.
"Medium Income":
Annual income between $51,000 and $100,000.
"High Income":
Annual income > $100,000.
Spending Score Categories:


Formula: 
=IF(SpendingScore >= 80, "High Spender", IF(SpendingScore >= 50, "Medium Spender", "Low Spender"))
--------------------------------------------------------------------------------------------------------------------------------------------
Categories:

"High Spender": 
Spending score ≥ 80.
"Medium Spender": 
Spending score between 50 and 79.
"Low Spender": 
Spending score < 50.

Segmentation Logic
Combined income and spending behavior to create customer segments:

Loyal High-Value Customers: 
High-income customers with high spending scores.
Formula:
=IF(AND(AnnualIncome > 100, SpendingScore > 80), "Loyal High-Value Customer", "Other")
Budget-Friendly High Spenders:
Low-income customers with high spending scores.
Formula: 
=IF(AND(AnnualIncome <= 50, SpendingScore > 80), "Budget-Friendly High Spender", "Other")
Insights Derived Using SUMIF
Used SUMIF to calculate totals for each segment:

Total spending score for Loyal High-Value Customers:
Formula: 
=SUMIF(SegmentRange, "Loyal High-Value Customer", SpendingScoreRange)
Total income for Medium Spenders:
Formula:
=SUMIF(SpendingScoreRange, "Medium Spender", IncomeRange)

3. Data Visualization
Created visualizations to communicate insights effectively:

Scatter Plot: 
Compared Annual Income vs. Spending Score to identify patterns in customer behavior.
Bar Chart:
Displayed the distribution of customers across spending categories.
Used COUNTIF() to count customers in each category.
Formula:
=COUNTIF(SpendingScoreRange, "High Spender")
Histogram:
Showed the distribution of Annual Income and Spending Score values.
Conditional Formatting:
Highlighted high-income, high-spending customers in the dataset.

--------------------------------------------------------------------------------------------------------------------------------------------
Key Insights
Segment Characteristics:

High-income, high-spending customers (VIPs) make up a small but lucrative portion of the customer base.
Budget-friendly high spenders are a significant group that could be targeted with discounts and promotions.
Income vs. Spending Patterns:

Higher income generally correlates with higher spending, but some low-income customers exhibit unexpectedly high spending behavior.
--------------------------------------------------------------------------------------------------------------------------------------------

Marketing Recommendations:

Focus on loyalty programs for Loyal High-Value Customers.
Offer discounts and budget-friendly promotions for Budget-Friendly High Spenders.
Incentivize occasional shoppers to spend more by offering targeted promotions.
Challenges and Learnings

Outlier Detection:

Learned how to calculate and interpret IQR values.
Practiced implementing Excel formulas to automate boundary calculations.

--------------------------------------------------------------------------------------------------------------------------------------------
Excel Skills:

Gained proficiency in functions like SUMIF(), IF(), COUNTIF(), and QUARTILE().
Improved skills in creating advanced visualizations to highlight trends.

Manual Clustering Approximation:

Experimented with manually simulating clustering (K-means) by categorizing data into 3 clusters based on income and spending score.
Tools and Skills Used
Microsoft Excel:
Functions: 
SUMIF, IF, COUNTIF, QUARTILE, CORREL.
Data cleaning, transformation, and analysis.
Visualizations: 
Scatter plots, bar charts, histograms, and conditional formatting.
--------------------------------------------------------------------------------------------------------------------------------------------
Soft Skills:
Problem-solving and data-driven decision-making.
Effective documentation and reporting.

Next Steps
Expand the analysis using Python or R for automated clustering (e.g., K-means).
Explore machine learning techniques for deeper insights.
Refine visualizations for presentations using Power BI or Tableau.
Project Files

File Name	Description
Mall_Customers.csv	Raw dataset used for the analysis.
Customer_Segmentation.xlsx	Excel file with calculations and visualizations.
README.md	Detailed project documentation.
Acknowledgments
Dataset sourced from Kaggle: Mall Customers Dataset.
