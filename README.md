# 📊 Tata Data Visualisation — Empowering Business with Effective Insights

## 📌 Project Overview

This project was completed as part of the **Tata Data Visualisation: Empowering Business with Effective Insights** job simulation on **Forage**.

The project simulates a business analytics scenario where retail transaction data is analyzed and transformed into meaningful visualizations for business decision-making.

The analysis focuses on the requirements of two key stakeholders:

- 👔 **CEO** — Revenue trends, business performance, geographic markets and expansion opportunities
- 📢 **CMO** — Country performance, sales quantity and high-value customers

The project demonstrates how raw transactional data can be converted into business insights using **Tableau**.

### The simulation focused on four key areas:

1. Framing the Business Scenario
2. Choosing the Right Visuals
3. Creating Effective Visuals
4. Communicating Insights and Analysis

---

## 🎯 Business Objective

The objective of this project was to analyze online retail transaction data and create visualizations that help management understand:

- Monthly revenue trends
- Seasonal revenue patterns
- Top-performing countries
- Sales quantity across countries
- Highest-value customers
- Geographic business performance
- Potential market opportunities

The overall analytical workflow was:

```text
Raw Retail Data
       ↓
Data Preparation
       ↓
Business Questions
       ↓
Data Analysis
       ↓
Tableau Visualization
       ↓
Business Insights
       ↓
Recommendations
```
## 🧩 Project Architecture
<img width="952" height="354" alt="image" src="https://github.com/user-attachments/assets/2dff6875-c7ca-4daa-b3fe-c777f2c35caa" />

## 🗂️ Dataset  

The project uses an Online Retail transaction dataset containing fields such as:
```text
Field	Description
Invoice No    Transaction / invoice identifier
Stock Code    Product identifier
Description   Product description
Quantity      Number of units purchased
Invoice Date  Date and time of transaction
Unit Price    Price per unit
Customer ID   Customer identifier
Country       Customer's country
Revenue       Revenue generated from the transaction
```

## 🧹 Data Preparation  

Before performing the analysis, transaction data should be checked for records that could distort the results.  

Important validation areas include:

```text
Negative quantities
Invalid unit prices
Returned transactions
Missing customer information
Incorrect or incomplete records
```
The analysis focuses on valid transaction records so that revenue and quantity calculations provide meaningful business results.  

## 📊 QUESTION 1 — Revenue by Month, 2011
### 📌 **Business Question**  
The CEO wants to view the time series of revenue for the year 2011, with monthly-level detail, in order to understand revenue patterns and seasonal trends.  
  
### 🛠️ **Tableau Solution**  
Chart Type:-Line Chart  
Tableau Configuration  
```text
Columns → MONTH(Invoice Date)

Rows → SUM(Revenue)

Filter → YEAR(Invoice Date) = 2011
```
**Main Fields Used**  
```text
Invoice Date
Revenue
```
### 📸 **Solution Screenshot**  

<img width="1918" height="1000" alt="image" src="https://github.com/user-attachments/assets/636c6748-73ad-48f8-8623-863423d99cdc" />  
  
### 📈 **Results**  
```text
Month         Revenue
January       $0.69M
February      $0.52M
March         $0.72M
April         $0.54M
May           $0.77M
June          $0.76M
July          $0.72M
August        $0.76M
September     $1.06M
October       $1.15M
November      $1.51M
December      $0.64M
```

### 💡 **Key Insight**  

Revenue remained relatively moderate during the first part of 2011 but increased significantly from September onwards.  
The highest monthly revenue was:  

November — approximately $1.51M  

There was then a significant decline in December to approximately $0.64M.  

### 🎯 **Business Recommendation**  
The business should investigate the factors behind the strong September–November performance. 

Possible areas for further analysis include:  
```text
Seasonal purchasing behavior
Marketing campaigns
Promotions
Product demand
Customer purchasing patterns
Holiday-related shopping
```

## 🌍 QUESTION 2 — Top 10 Countries by Revenue & Quantity

### 📌 Business Question

The CMO wants to identify the top 10 countries generating the highest revenue and compare their sales quantity, while excluding the United Kingdom.  

### 🛠️ Tableau Solution  

Chart Type:- Grouped Bar Chart & Tableau Configuration  
```text
Columns → Country + Measure Names        
Rows → Measure Values        
Measures:
       SUM(Quantity)
       SUM(Revenue)  
Filters:
       Country
       Measure Names  
```
### 📸 Solution Screenshot  
 <img width="1905" height="1006" alt="image" src="https://github.com/user-attachments/assets/649a1645-5eb4-473f-afbf-21ef96dadfe9" />  


### 🌎 Countries Highlighted  

The visualization identifies the following major markets:  
```text
Netherlands
Ireland
Germany
France
Australia
Spain
Switzerland
Sweden
Belgium
Japan
```
### 💡 Key Insight  

The visualization compares Revenue and Quantity together.This is useful because a country with a high sales quantity does not necessarily generate the highest revenue.
The difference between revenue and quantity can help management investigate:  
```text
Product mix
Order size
Customer purchasing behavior
Average transaction value
Market characteristics
```
### 🎯 Business Recommendation  

The CMO can use this analysis to identify international markets that may deserve additional attention.  

Potential actions include:  
```text
Targeted marketing campaigns
Customer acquisition
Localized promotions
Product expansion
Increased advertising investment
```
## 👥 QUESTION 3 — Top 10 Customers by Revenue
### 📌 Business Question 

The CMO wants to identify the top 10 customers by revenue, with the highest revenue-generating customer shown first.

### 🛠️ Tableau Solution  

Chart Type:- Horizontal Bar Chart  

Tableau Configuration

       Rows → Customer ID
       Columns → SUM(Revenue)
       Filter → Top 10 Customers by Revenue
       Sort → Descending by Revenue
### 📸 Solution Screenshot  

<img width="1915" height="1009" alt="image" src="https://github.com/user-attachments/assets/363ee575-51ac-4020-b37b-a88ed6544de6" />

### 📈 Results  
```text
Rank	Customer ID	Revenue
1	14646         $280.21K  
2	18102         $259.66K  
3	17450         $194.55K  
4	16446         $168.47K
5	14911         $143.83K
6	12415         $124.91K
7	14156         $117.38K
8	17511         $91.06K
9	16029         $81.02K
10	12346         $77.18K
```
### 💡 Key Insight  

Customer 14646 is the highest-revenue customer in the visualization, generating approximately: $280.21K  
Customer 18102 is the second-highest, generating approximately: $259.66K  
The top 10 customers shown in the worksheet collectively contribute approximately $1.54M in revenue.  

### 🎯 Business Recommendation  

High-value customers should be considered a priority for retention and relationship management.  

Potential strategies include:  

       VIP customer programs
       Personalized offers
       Loyalty rewards
       Customer retention campaigns
       Cross-selling
       Upselling
       Personalized communication
  

## 🗺️ QUESTION 4 — Revenue by Country  
### 📌 Business Question  

The fourth visualization provides a geographic view of country-level business performance and helps management understand where revenue is being generated.  

### 🛠️ Tableau Solution  
Chart Type:-Geographic Map  

Tableau Configuration  

       Columns → Longitude (generated)
       Rows → Latitude (generated)
       Detail → Country
       Color → SUM(Revenue)
       Filter → Country
       
### 📸 Solution Screenshot  
<img width="1918" height="1006" alt="image" src="https://github.com/user-attachments/assets/5adb2f1a-5ab1-4450-82c7-3c8a3c5ac8e9" />


### 💡 Key Insight  

A geographic visualization makes it easier to understand how business performance is distributed across countries.  
Instead of analyzing countries individually in a table, management can visually identify geographic areas with stronger business activity.  
This can support further investigation into:  
       
       International market performance
       Revenue concentration
       Geographic opportunities
       Marketing priorities
       Market expansion
       
### 🎯 Business Recommendation  

The business can combine geographic performance with other factors such as:  

       Market size
       Customer growth
       Sales quantity
       Revenue
       Competition
       Logistics
       Product demand



## 📊 Overall Business Insights

The four visualizations provide several important observations.

💰 1. Revenue shows a strong late-year increase

The monthly revenue analysis shows a significant increase from September to November, with November reaching approximately $1.51M.

🌍 2. International markets have different performance profiles

Comparing revenue and quantity allows management to understand that sales volume and revenue are not necessarily proportional.

👥 3. High-value customers contribute significant revenue

The Top 10 customer analysis identifies customers that have a substantial impact on revenue generation.

🗺️ 4. Geographic analysis supports market evaluation

The country map provides an intuitive way to understand where the business generates revenue.

🎯 5. Business questions should drive visualization selection

Different business questions require different visualization techniques.

Revenue Trend
     ↓
Line Chart

Country Comparison
     ↓
Grouped Bar Chart

Customer Ranking
     ↓
Horizontal Bar Chart

Geographic Analysis
     ↓
Map
💡 Overall Business Recommendations

Based on the analysis, management could consider the following actions.

1. Investigate seasonal revenue patterns

Study why revenue increases significantly during September–November and determine whether similar strategies can be used in future years.

2. Focus on high-performing international markets

Use revenue and quantity analysis to identify countries that could benefit from additional marketing investment.

3. Strengthen customer retention

Develop personalized strategies for high-value customers to improve retention and lifetime value.

4. Evaluate expansion opportunities

Use geographic analysis as an initial screening tool before conducting detailed market research.

5. Monitor customer concentration

Track the contribution of high-value customers to total revenue and develop strategies to reduce dependency risk.

🖥️ Professional Dashboard Approach

The project follows a stakeholder-focused analytical flow:

┌──────────────────────────┐
│     REVENUE TREND        │
│      Question 1          │
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│    MARKET PERFORMANCE    │
│      Question 2          │
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│     CUSTOMER VALUE       │
│      Question 3          │
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│   GEOGRAPHIC ANALYSIS    │
│      Question 4          │
└────────────┬─────────────┘
             ↓
┌──────────────────────────┐
│ BUSINESS INSIGHTS &      │
│ RECOMMENDATIONS          │
└──────────────────────────┘

This approach helps move from:

How is the business performing?

to:

Where is the business performing?

to:

Who is generating the revenue?

to:

Which markets should be investigated further?

🎨 Visualization Design

The project demonstrates the principle:

Choose the visualization based on the business question.

Business Question	Visualization	Purpose
Monthly revenue trend	Line Chart	Identify trends and seasonality
Country comparison	Grouped Bar Chart	Compare revenue and quantity
Customer ranking	Horizontal Bar Chart	Rank high-value customers
Geographic performance	Map	Understand geographic distribution
🛠️ Tools & Technologies
Visualization
Tableau Desktop
Data Analysis
Data Cleaning
Exploratory Data Analysis
Data Aggregation
Filtering
Sorting
Top-N Analysis
Time-Series Analysis
Geographic Analysis
Business Intelligence
KPI Analysis
Revenue Analysis
Customer Analysis
Market Analysis
Data Storytelling
Stakeholder Analysis
Business Decision Support
🧠 Skills Demonstrated
✓ Tableau
✓ Data Visualization
✓ Business Intelligence
✓ Data Analysis
✓ Data Cleaning
✓ Exploratory Data Analysis
✓ Revenue Analysis
✓ Customer Analysis
✓ Geographic Analysis
✓ Trend Analysis
✓ Data Storytelling
✓ Business Analysis
✓ Stakeholder Requirement Analysis
✓ Executive Reporting
✓ Insight Communication
📁 Repository Structure
Tata-Data-Visualisation-Forage/
│
├── README.md
│
├── Dashboard/
│   └── Tata_Retail_Analysis.twbx
│
├── Screenshots/
│   ├── Question_1_Revenue_by_Month.png
│   ├── Question_2_Top_Countries.png
│   ├── Question_3_Top_Customers.png
│   └── Question_4_Revenue_by_Country.png
│
├── Data/
│   └── Online_Retail_Data.xlsx
│
└── Documentation/
    └── Project_Insights.md
🏆 Forage Job Simulation
Program

Tata Data Visualisation: Empowering Business with Effective Insights

Platform

Forage

Completion

August 2026

Primary Tool

Tableau Desktop

Practical Areas Covered
Framing the Business Scenario
Choosing the Right Visuals
Creating Effective Visuals
Communicating Insights and Analysis
📜 Certificate

The project was completed as part of the Tata Data Visualisation job simulation on Forage.

Certificate:

Certificate/Tata_Forage_Certificate.pdf

🚀 Project Takeaway

This project demonstrates how a Data Analyst can transform transactional retail data into business-focused insights.

The key lesson is that effective data analytics is not only about creating charts.

It is about:

Understanding the Business Question
             ↓
Selecting the Right Data
             ↓
Choosing the Right Visualization
             ↓
Finding Meaningful Patterns
             ↓
Communicating the Insight
             ↓
Supporting Business Decisions
👨‍💻 Author
Shubham Singh

Data Analyst | Business Intelligence | Data Visualization

Areas of Interest
Data Analytics
Business Intelligence
Tableau
Power BI
SQL
Data Visualization
Business Analytics
Data Storytelling
⭐ If you found this project useful

Feel free to star ⭐ the repository and explore the visualizations.



