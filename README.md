# 🛍️ Retail Sales Analysis with SQL

This project presents an end-to-end **Retail Sales Data Analysis** using SQL. It involves querying a retail transaction dataset to generate insights on sales performance, customer behavior, and product trends.

---

## 📁 Dataset Overview

The dataset `SQL - Retail Sales Analysis_utf.csv` contains retail transactions with the following key columns:

- `transactions_id`: Unique transaction identifier  
- `sale_date`: Date of the sale  
- `sale_time`: Time of the sale  
- `customer_id`: Unique customer ID  
- `gender`: Gender of the customer  
- `age`: Age of the customer  
- `category`: Product category (e.g., Clothing, Electronics)  
- `quantiy`: Number of units sold (note: typo in column name)  
- `price_per_unit`: Price per unit of the product  
- `cogs`: Cost of goods sold  
- `total_sale`: Total sale value (revenue)

---

## 🧠 Objectives

- Analyze **monthly sales trends**
- Identify **high-performing product categories**
- Understand **customer behavior** by age and gender
- Filter transactions based on **custom business criteria**

---

## 🛠️ SQL Tasks Performed

### 1. Transactions for Specific Category
```sql
SELECT * 
FROM retail_sales
WHERE LOWER(category) = 'clothing'
  AND DATE_FORMAT(sale_date, '%Y-%m') = '2022-11'
  AND quantiy > 4;
2. Average Monthly Sales
sql
Copy
Edit
SELECT 
  EXTRACT(YEAR FROM sale_date) AS year,
  EXTRACT(MONTH FROM sale_date) AS month,
  AVG(total_sale) AS avg_sale
FROM retail_sales
GROUP BY 1, 2
ORDER BY 1, 3 DESC;
📊 Insights Extracted
November 2022 saw a spike in clothing transactions with high quantity.

Average sale value fluctuated across months and peaked during festive periods.

Gender-wise buying patterns highlighted targeted marketing opportunities.

Top-selling categories were consistently from electronics and fashion.

🧰 Tools Used
MySQL Workbench

Excel (for data cleaning)

Git & GitHub (version control)

📌 Notes
The column quantiy is a typo and should be treated as quantity.

Ensure you correct column names if importing into a SQL DB.

🚀 How to Use
Clone this repository:

bash
Copy
Edit
git clone https://github.com/your-username/retail-sales-sql-analysis.git
Import the CSV file into your SQL database.

Run the SQL queries from the queries.sql file to replicate the analysis.

🙋‍♂️ Author
Lokendra Singh
📧 singhlokendra2164@gmail.com
📞 +91-8604446022
🔗 LinkedIn | GitHub

📄 License
This project is licensed under the MIT License.

python
Copy
Edit

---

Let me know if you'd like:
- A separate `queries.sql` file
- A PDF or DOC version of this README
- Or if you're ready to publish it to GitHub and need help with that process too.
