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

**Solution 1: Using `OR` and `IS NULL`**  
```sql
SELECT name  
FROM Customer  
WHERE referee_id != 2 OR referee_id IS NULL;
```

**Solution 2: Using `COALESCE`**
```sql
SELECT name  
FROM Customer  
WHERE COALESCE(referee_id, 0) <> 2;
```

### [### 595 – Big Countries](https://leetcode.com/problems/big-countries/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
SELECT name, population, area
FROM World
WHERE area >= 3000000 OR population >= 25000000;
```

### [### 1148 – Article Views 1](https://leetcode.com/problems/article-views-i/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
SELECT DISTINCT author_id AS id
FROM Views
WHERE author_id = viewer_id
ORDER BY id ASC;
```

### [### 1683 – Invalid Tweets](https://leetcode.com/problems/invalid-tweets/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
SELECT tweet_id
FROM Tweets
WHERE LENGTH(content) > 15
```

### [### 1378 – Replace Employee ID With The Unique Identifier](https://leetcode.com/problems/replace-employee-id-with-the-unique-identifier/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
SELECT EmployeeUNI.unique_id, Employees.name
FROM Employees
LEFT JOIN EmployeeUNI ON Employees.id = EmployeeUNI.id
```

### [### 1068 – Product Sales Analysis I](https://leetcode.com/problems/product-sales-analysis-i/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
SELECT Product.product_name, Sales.year, Sales.price
FROM Sales
LEFT JOIN Product on Sales.product_id = Product.product_id
```