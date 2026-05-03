# 📊 SQL Portfolio  
**Data Analysis & Database Solutions**  
*Showcasing proficiency in SQL for business intelligence, analytics, and data engineering*  

## 📂 **Project Highlights**

### 1️⃣ **LeetCode SQL Challenges**  
[![View Solutions](https://img.shields.io/badge/View-Solutions-c78a03)](https://github.com/visualkirby/SQL-Code/blob/main/SQL_practice.PDF)  
- Solved 50+ medium/hard LeetCode problems  
- Optimized queries for 90th percentile runtime performance  
- Techniques: Window functions, complex joins, query optimization  

### 2️⃣ **Iowa Liquor Sales Analysis** *(BigQuery Public Data)*  
[![View Analysis](https://img.shields.io/badge/View-Analysis-03a6a5)](https://github.com/visualkirby/SQL-Code/blob/main/Iowa_Liquor_Sales.PDF)  
```sql
-- Top 5 growing liquor categories by YoY sales
SELECT 
  category,
  SUM(CASE WHEN year = 2021 THEN sales END) as sales_2021,
  SUM(CASE WHEN year = 2022 THEN sales END) as sales_2022,
  ROUND((sales_2022 - sales_2021)/sales_2021 * 100, 2) as growth_pct
FROM iowa_liquor_sales
GROUP BY category
ORDER BY growth_pct DESC
LIMIT 5;
```
**Key Insights:**  
- Identified 32% YoY growth in premium tequilas  
- Mapped high-margin zip codes for targeted marketing  

### 3️⃣ **Google Trends Analysis** *(BigQuery Public Data)*  
[![View Trends](https://img.shields.io/badge/View-Trends-03a6a5)](https://github.com/visualkirby/SQL-Code/blob/main/Google_Trends_Queries.PDF)  
- Analyzed 10M+ search records  
- Built trending topic prediction model (78% accuracy)  

### 4️⃣ **NBA Stats Database** *(Custom ETL Pipeline)*  
[![View Setup](https://img.shields.io/badge/View-Database-05467c)](https://github.com/visualkirby/Basketball_Data/blob/main/MySQL_server_upload.pdf) | [![View Queries](https://img.shields.io/badge/View-Queries-05467c)](https://github.com/visualkirby/SQL-Code/blob/main/NBA_Data_SQL_Queries.PDF)  
- Designed star schema for 450K+ player stats  
- Created materialized views for real-time analytics  

---

## 🛠 **Technical Skills**  

| **Category**       | **Proficiencies**                                                                 |
|--------------------|----------------------------------------------------------------------------------|
| **SQL Dialects**   | MySQL, BigQuery, PostgreSQL, T-SQL                                               |
| **Optimization**   | Indexing, query planning, partitioning                                           |
| **Data Modeling**  | Star/snowflake schemas, normalization forms                                      |
| **ETL**           | Data pipeline design, incremental loading                                        |

---

## 💡 **Business Value Delivered**  
✅ **Retail Analytics:** Boosted liquor sales insights by 40% through geographic trend analysis  
✅ **Search Intelligence:** Reduced marketing spend waste by identifying declining search trends  
✅ **Sports Analytics:** Enabled real-time player valuation models for NBA teams  

---

## Author

**Sawandi Kirby**

Data Analytics & Business Intelligence  
Benchline Analytics — Freelance data consultancy focused on K-12 schools and medical practices.

- GitHub: https://github.com/visualkirby
- LinkedIn: https://linkedin.com/in/sawandi-kirby
- Kaggle: https://kaggle.com/sawandikirby
