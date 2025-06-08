# Task-7-Sales_Summary
Sales Summary from a Tiny SQLite Database using Python

## Tools Used:
- Python (in Google Colab)
- SQLite (`sqlite3` library)
- pandas
- matplotlib

##  What I Did (Step-by-Step):

1. **Created an SQLite database** named `sales_data.db` inside the Python script.
2. **Created a `sales` table** with columns: `product`, `quantity`, and `price`.
3. **Inserted sample data** for products like Soap, Shampoo, Toothpaste, etc.
4. **Used SQL** to calculate:
   - Total quantity sold for each product
   - Total revenue (`quantity * price`)
5. **Loaded the SQL output into a pandas DataFrame**.
6. **Printed the sales summary table** using `print(df)`.
7. **Plotted a bar chart** to visualize revenue by product using `matplotlib`.
8. **Saved the chart** as `sales_chart.png`.

## SQL Query Used:

```sql
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product;
