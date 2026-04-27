

# Credit Card Transaction & Customer Analysis - Power BI Dashboard

## Project Overview

This project presents an end-to-end **Credit Card Analytics Dashboard** built using **Power BI**, backed by a **MySQL** database. It provides real-time insights into credit card transactions, customer demographics, revenue trends, and satisfaction scores,enabling data-driven decision making for financial stakeholders.

---

## Tech Stack

| Tool | Purpose |
|---|---|
| **MySQL** | Data storage and management |
| **Power BI Desktop** | Dashboard creation and visualization |
| **Power Query (M Language)** | Data transformation and cleaning |
| **DAX** | Calculated measures and KPIs |
| **CSV / Excel** | Raw data import source |

---

## Dashboard Pages

### 1. Credit Card Transaction Report
Focuses on transaction-level metrics:
- **QTR Revenue & Transaction Volume** **:** Q1 to Q4 trend analysis.
- **Revenue by Expenditure Type** **:** Bills, Entertainment, Fuel, Grocery, Food, Travel.
- **Revenue by Education Level** **:** Graduate, High School, Post-Graduate, Doctorate, etc.
- **Revenue by Customer Job** **:** Businessman, White-collar, Self-employed, Govt, Blue-collar, Retirees.
- **Revenue by Card Category** **:** Blue, Silver, Gold, Platinum.
- **Revenue by Use Chip** **:** Swipe, Chip, Online.

### 2. Credit Card Customer Report
Focuses on customer demographic insights:
- **Revenue by Age Group** **:** 0-30, 30-40, 40-50, 50-60, 60+
- **Revenue by Income Group** **:** High, Medium, Low
- **Revenue by State** **:** TX, NY, CA, FL, NJ
- **Revenue by Marital Status** **:** Married, Single, Unknown
- **Revenue by Education Level**
- **Revenue by Dependent Count**
- **Revenue by Week** **:** Weekly trend across Jan–Oct 2023
- **Gender Split** **:** Male vs Female revenue comparison

---

## Key KPIs

| Metric | Value |
|---|---|
| Total Revenue | **57M** |
| Total Transaction Amount | **46M** |
| Total Interest Earned | **7.98M** |
| Transaction Count | **667K** |
| Total Income | **588M** |
| Customer Satisfaction Score | **3.19** |

---

## Key Insights

- **Blue card** dominates revenue at **47M**, far ahead of Silver (5.6M), Gold (2.5M), and Platinum (1.1M)
- **Swipe transactions** generate the highest revenue (**36M**) compared to Chip (17M) and Online (4M)
- **Businessmen** are the top revenue-generating job category at **17.7M**
- **Graduate customers** contribute the most revenue at **23M**
- **Bills** is the highest expenditure type generating **14M** in revenue
- **Q4** shows the highest quarterly revenue at **14.5M**
- **Male customers** generate more revenue (**31M**) compared to female (**26M**)
- **Age group 40-50** is the highest revenue-generating age bracket at **14M**
- **High income group** customers contribute **23M** in revenue

---

## Database Setup (MySQL)

```sql
CREATE TABLE credit_card(
    Client_Num INT PRIMARY KEY,
    Card_Category VARCHAR(20),
    Total_Trans_Amt DECIMAL(10,2),
    Total_Trans_Vol INT,
    Revenue DECIMAL(10,2),
    Interest_Earned DECIMAL(10,2),
    Use_Chip VARCHAR(20),
    Expenditure_Type VARCHAR(30),
    Week_Start_Date DATE
);

-- Import data from CSV
LOAD DATA INFILE 'path/to/data.csv'
INTO TABLE credit_card
FIELDS TERMINATED BY ','
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS;
```

---
## Power BI to MySQL Connection Steps



**Step 1** **:** Open Power BI Desktop

**Step 2** **:** Go to Home → Get Data → MySQL Database

**Step 3** **:** Enter server and database credentials

**Step 4** **:** Select required tables and load

**Step 5** **:** Use Power Query Editor to clean and transform data

**Step 6** **:** Build visuals and publish


---

---

## Conclusion & Key Insights

This dashboard delivers a **360° view of credit card operations** by combining transaction-level data with customer demographics. Transforming raw MySQL data into boardroom-ready intelligence.

**Week-on-Week (WoW) Performance:**

**WoW Revenue** grew by **28.8%**, signaling strong upward momentum in card usage and customer spending behavior.

**Year-to-Date (YTD) Business Impact:**

- Total revenue reached **57M** with total interest earnings of **8M** reflecting strong portfolio profitability
- **Blue & Silver cards together account for 93% of all transactions**, making them the backbone of the credit card business
- **Male customers drive 54% of revenue (31M)** vs **female (26M)**, highlighting a key demographic targeting opportunity.
- **TX, NY & CA alone contribute 68% of total revenue** : geographic concentration that can guide regional marketing strategies
- **Activation rate stands at 57.5%** **:** indicating nearly half of issued cards remain inactive, a critical area for customer engagement campaigns
- **Delinquency rate is 6.06%** **:** a risk metric that needs monitoring to reduce defaults and protect revenue
- Total transaction volume hit **46M** with **667K transactions** processed successfully across all card categories

> These insights can directly support business decisions around **customer acquisition, risk management, regional expansion, and card portfolio optimization.**
