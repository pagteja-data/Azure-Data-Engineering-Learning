# SQL Joins
## What is a Join?
A JOIN combines rows from two or more tables based on a related column.
## Types of Joins
### 1. INNER JOIN
Returns matching records from both tables.
```sql
SELECT c.customer_id,
      c.customer_name,
      o.order_id
FROM Customers c
INNER JOIN Orders o
ON c.customer_id = o.customer_id;
```
### Use Case
Used to retrieve customers who have placed orders.
---
### 2. LEFT JOIN
Returns all records from the left table and matching records from the right table.
```sql
SELECT c.customer_name,
      o.order_id
FROM Customers c
LEFT JOIN Orders o
ON c.customer_id = o.customer_id;
```
### Use Case
Find customers who haven't placed any orders.
---
### 3. RIGHT JOIN
Returns all records from the right table.
---
### 4. FULL OUTER JOIN
Returns all matching and non-matching rows.
---
### 5. CROSS JOIN
Returns every possible combination.
---
## Real Data Engineering Example
Joining Customer and Account tables during ETL to create a customer profile dataset.
## Interview Question
**Q:** Difference between INNER JOIN and LEFT JOIN?
**Answer:**
- INNER JOIN returns only matching rows.
- LEFT JOIN returns all rows from the left table and matching rows from the right table.
