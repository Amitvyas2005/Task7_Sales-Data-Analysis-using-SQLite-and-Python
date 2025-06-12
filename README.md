
# 📊 Sales Data Analysis using SQLite and Python

## Overview

This Python script (Task7_SQLiteDatabase_using_Python.py) connects to an SQLite database (sales_data.db) to perform various SQL queries for analyzing sales data. It uses the pandas library to process query results and matplotlib to create visualizations. The script calculates key metrics such as total sales, total profit, total quantity sold, total orders, and provides insights into sales by product, profit by payment mode, orders by state, and quantity sold over time.
---

## 🔧 Technologies Used

- **Python**
- **SQLite** (`sqlite3`)
- **Pandas**
- **Matplotlib**

---

## 📂 Files

- `Task7_SQLiteDatabase_using_Python.ipynb` - Main script for querying and analyzing the sales database.
- `Created_SQLiteDatabase_using_Python.ipynb`  - Assumed SQLite database file with a table named `sales`.
- `sales.db`-created by using jupyter notebook
- `Visualizations.pdf` - All visuals generated using quries.
- `Original_Sales_Dataset.csv`

---

## 📈 Features

The script connects to a local SQLite database and runs multiple queries to extract insights:

### 📌 SQL Analysis Queries

1. **Total Sales**
   ```sql
   SELECT SUM(amount) AS total_sales FROM sales;
   ```

2. **Total Profit**
   ```sql
   SELECT SUM(profit) AS total_profit FROM sales;
   ```

3. **Total Quantity Sold**
   ```sql
   SELECT SUM(quantity) AS total_quantity FROM sales;
   ```

4. **Total Orders**
   ```sql
   SELECT COUNT("Order ID") AS total_orders FROM sales;
   ```

5. **Sales by Product**
   ```sql
   SELECT Product_Name, SUM(Amount) AS total_sales 
   FROM sales 
   GROUP BY Product_Name 
   ORDER BY total_sales DESC;
   ```

6. **Profit by Payment Mode**
   ```sql
   SELECT PaymentMode, SUM(Profit) AS total_profit 
   FROM sales 
   GROUP BY PaymentMode 
   ORDER BY total_profit DESC;
   ```

7. **Orders by State**
   ```sql
   SELECT State, COUNT("Order ID") AS total_orders 
   FROM sales 
   GROUP BY State 
   ORDER BY total_orders DESC;
   ```

8. **Monthly Quantity Trend**
   ```sql
   SELECT "Year-Month", SUM(Quantity) AS total_quantity 
   FROM sales 
   GROUP BY "Year-Month" 
   ORDER BY "Year-Month";
   ```
---
## 🎯 Conclusion

This project successfully demonstrates sales data analysis using Python, SQLite, and Pandas, delivering key insights through 8 SQL queries and 4 visualizations. It provides a clear, efficient approach to extracting and visualizing business metrics, showcasing the power of data-driven decision-making.
