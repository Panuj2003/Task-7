Task 7 – Basic Sales Summary using SQLite + Python

##  Objective  
Create a small SQLite database using Python, insert sample sales data, run SQL queries for summary, and visualize the results using a simple bar chart.

##  Tools Used  
- Python  
- sqlite3 (built-in, no installation required)  
- Pandas  
- Matplotlib  


##  What This Task Does

### 1) Creates a SQLite database (`sales_data.db`)
A table named **sales** is created with:
- product  
- quantity  
- price  

###  2) Inserts sample data
Products used:
- Laptop  
- Phone  
- Headphones  

Each with different quantities and prices.

##  SQL Query Used
The main SQL query for this task:

```sql
SELECT 
    product,
    SUM(quantity) AS total_quantity,
    SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;
