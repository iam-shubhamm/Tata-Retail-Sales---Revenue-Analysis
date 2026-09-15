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

# 🎯 Business Objective

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
# 🧩 Project Architecture
<img width="952" height="354" alt="image" src="https://github.com/user-attachments/assets/2dff6875-c7ca-4daa-b3fe-c777f2c35caa" />

# 🗂️ Dataset

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

# 🧹 Data Preparation

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

# 📊 QUESTION 1 — Revenue by Month, 2011
📌 Business Question

The CEO wants to view the time series of revenue for the year 2011, with monthly-level detail, in order to understand revenue patterns and seasonal trends.
🛠️ Tableau Solution
Chart Type

Line Chart

Tableau Configuration
```text
Columns → MONTH(Invoice Date)

Rows → SUM(Revenue)

Filter → YEAR(Invoice Date) = 2011
```
Main Fields Used
```text
Invoice Date
Revenue
```
📸 Solution Screenshot
<img width="1918" height="1000" alt="image" src="https://github.com/user-attachments/assets/636c6748-73ad-48f8-8623-863423d99cdc" />

📈 Results
Month	Revenue
January	$0.69M
February	$0.52M
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

💡 Key Insight

Revenue remained relatively moderate during the first part of 2011 but increased significantly from September onwards.
The highest monthly revenue was:

November — approximately $1.51M

There was then a significant decline in December to approximately $0.64M.

🎯 Business Recommendation
The business should investigate the factors behind the strong September–November performance.

Possible areas for further analysis include:
Seasonal purchasing behavior
Marketing campaigns
Promotions
Product demand
Customer purchasing patterns
Holiday-related shopping

Understanding these patterns could help the company plan future marketing and inventory strategies.



