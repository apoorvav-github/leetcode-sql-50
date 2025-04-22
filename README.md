# SQL 50 – LeetCode  
This repo contains solutions to the [SQL 50 Study Plan](https://leetcode.com/studyplan/top-sql-50/) on Leetcode.

---

### [1757 – Recyclable and Low Fat Products](https://leetcode.com/problems/recyclable-and-low-fat-products/?envType=study-plan-v2&envId=top-sql-50)
```sql
SELECT product_id
FROM Products
WHERE low_fats = 'Y'
AND recyclable = 'Y';
```

### [### 584 – Find Customer Referee](https://leetcode.com/problems/find-customer-referee/description/?envType=study-plan-v2&envId=top-sql-50)

**Solution 1: Using OR and IS NULL**  
```sql
SELECT name  
FROM Customer  
WHERE referee_id != 2 OR referee_id IS NULL;
```

**Solution 2: Using COALESCE**
```sql
SELECT name  
FROM Customer  
WHERE COALESCE(referee_id, 0) <> 2;
```