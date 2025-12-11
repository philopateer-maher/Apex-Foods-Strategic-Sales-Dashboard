# 🥗 Apex Foods: Strategic Business Analysis Dashboard

![Apex Foods Logo](path-to-your-logo-image.png)
*(Replace this text with your dashboard screenshot or logo)*

## 📖 Project Overview
**Apex Foods** is a global food distributor facing challenges in tracking revenue growth, managing inventory levels, and optimizing shipping costs. This Power BI project transforms raw data into actionable insights, enabling the executive team to monitor performance across Sales, Products, Customers, Employees, and Logistics.

* **Tools Used:** Power BI, DAX, Power Query.
* **Dataset:** Northwind Traders (Expanded & Customized).
* **Data Model:** Star Schema (Facts & Dimensions).

---

## 📊 Dashboard Structure (5 Pages)

### 1. Executive Sales Management
**Goal:** High-level revenue tracking and year-over-year growth analysis.
* **Key Features:**
    * KPI Cards for Total Revenue, Profit, and YTD Growth.
    * Area Chart for Monthly Revenue Trends (Current Year vs. Last Year).
    * Dynamic Slicers for Year and Month filtering.

### 2. Product Portfolio & Inventory
**Goal:** Identify high-performing products and prevent stockouts.
* **Key Features:**
    * **Scatter Plot:** Price vs. Volume analysis to identify "Cash Cows" and "Star Products."
    * **Inventory Report:** Automated "Low Stock" alerts using conditional formatting (Red flags when Stock < Reorder Level).
    * **Tree Map:** Revenue distribution by Product Category.

### 3. Customer Insights
**Goal:** Understand customer geography and purchasing behavior.
* **Key Features:**
    * **Global Shape Map:** Visualizing revenue by country.
    * **Top 10 Customers:** Ranked by Total Spend.
    * **Purchase Frequency:** Analysis of Active Customers and Average Revenue per Client.

### 4. Sales Team Performance
**Goal:** Evaluate employee efficiency and discounting behavior.
* **Key Features:**
    * **Performance Matrix:** Revenue vs. Discount % to identify reps who sell on value vs. price.
    * **Scatter Plot:** Revenue vs. Order Volume (Identifying high-efficiency sellers).
    * **Leaderboard:** Ranking sales representatives by total contribution.

### 5. Logistics & Operations
**Goal:** Optimize shipping costs and delivery times.
* **Key Features:**
    * **Freight Analysis:** Top 5 most expensive countries to ship to.
    * **Carrier Performance:** Comparing "Speedy Express" vs. "United Package" on delivery speed.
    * **Late Delivery Analysis:** Tracking percentage of orders shipped after the required date.

---

## 🛠 Technical Highlights

### Data Modeling
* Built a robust **Star Schema** with one Fact table (`OrderFact`) and five Dimension tables (`Customers`, `Products`, `Employees`, `Shippers`, `Calendar`).
* Ensured **1-to-Many relationships** to prevent cardinality issues and ensure accurate filtering.

### Advanced DAX Measures
Implemented complex calculations including:
* **Time Intelligence:** `TOTALYTD`, `SAMEPERIODLASTYEAR`, and Year-over-Year Growth %.
* **Dynamic Logic:** `COUNTROWS`, `CALCULATE`, and `SWITCH` for segmentation.
* **Inventory Logic:** Custom flags for reorder levels (`IF(UnitsInStock <= ReorderLevel, 1, 0)`).

### UI/UX Design
* **Custom Navigation Bar:** Vertical sidebar with hover effects for page navigation.
* **Conditional Formatting:** Dynamic color scales for Growth % (Green/Red) and Inventory Health.
* **Interactive Elements:** Drill-through filters, tooltips, and edited interactions to prevent slicer conflict.

---

## 🚀 How to Run This Project
1.  Download the `.pbix` file from this repository.
2.  Open the file in **Power BI Desktop**.
3.  Ensure the data source settings point to the included Excel/CSV files (if applicable) or explore the pre-loaded data model.

---
*Note: This project is based on the Northwind dataset, a standard dataset for business intelligence training.*
