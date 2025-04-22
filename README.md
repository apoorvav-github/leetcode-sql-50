# SQL 50 – LeetCode  
This repo contains solutions to the [SQL 50 Study Plan](https://leetcode.com/studyplan/top-sql-50/).

---

### [1757 – Recyclable and Low Fat Products](https://leetcode.com/problems/recyclable-and-low-fat-products/?envType=study-plan-v2&envId=top-sql-50)
```sql
SELECT product_id
FROM Products
WHERE low_fats = 'Y'
AND recyclable = 'Y';
