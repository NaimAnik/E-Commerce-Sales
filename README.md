## E-Commerce Sales and Profitability Analysis (SQL Project)

### 🎯 **Objective**
The primary objective of this project was to conduct a comprehensive analysis of an e-commerce store's transactional and sales target data to identify **key performance indicators (KPIs)**, measure profitability, and provide **data-driven insights** for business optimization.

### 💻 **Dataset Overview**
The analysis utilized an Indian E-commerce store dataset from Kaggle, comprising three key tables:

| Table Name | Key Data Points |
| :--- | :--- |
| `List of Orders` (Implied as `customers`) | Order ID, Date of Purchase, Customer Details |
| `Order Details` (Implied as `order_details`) | Order ID, Price, Quantity, Profit, Category, and Subcategory |
| `Sales Target` (Implied as `sales_target`) | Sales Target Amount and date for each product category |

### 🛠️ **Key SQL Techniques Demonstrated**
This project showcases proficiency across foundational and advanced SQL concepts, which are critical for data analysis roles:

* **Window Functions (`DENSE_RANK()`):** Used to identify the **Top 3 Profitable Sub-Categories** within each major product category.
* **Common Table Expressions (CTEs):** Used for code clarity, calculating **Total Revenue**, and determining the **Profit/Loss Status** of orders.
* **Conditional Logic (`CASE` Statements):** Used to categorize orders based on profit margins (Profit, Loss, or None).
* **Advanced Joins & Aggregation:** Utilized `JOIN` operations (e.g., to link customer state to order details) and aggregate functions (`SUM`, `COUNT`, `AVG`) to generate core metrics.

### 📊 **Core Business Questions & Insights**
The analysis covered a range of topics, including customer analysis, product pricing, revenue analysis, profitability analysis, and trend analysis.

| Analysis Area | Key Insight Delivered | SQL Query Example |
| :--- | :--- | :--- |
| **Profitability** | Determined the total profit generated for each category and identified the overall **TOP Profitable category**. | `SELECT Category, SUM(Profit) ... GROUP BY Category` |
| **Performance Ranking** | Identified the **Top 5 profitable cities** and the **Top 3 profitable sub-categories** using ranking functions. | `DENSE_RANK() OVER(PARTITION BY Category...)` |
| **Sales & Revenue** | Calculated the **Total Revenue Generated** by the store and the revenue generated per category. | `SELECT SUM(Sellprice) AS Total_Revenue` (using CTE) |
| **Customer Behavior** | Counted the number of **unique customers** and the distribution of orders state-wise. | `SELECT State, COUNT(Order_ID) ...` |

### **⭐ Next Steps**
The results from the SQL analysis can guide decision-making processes, such as optimizing inventory, setting sales targets, tailoring marketing strategies, and identifying areas of improvement to enhance overall performance and profitability.

The next step for this project would be to **visualize these key metrics** in a tool like Tableau or Power BI to create a dynamic business dashboard.
