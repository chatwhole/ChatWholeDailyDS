# 🗄️ SQL for Data Science

<p align="center">
  <img src="sql-cheat-sheet.svg" alt="SQL Cheat Sheet" width="100%">
</p>

## 📚 Table of Contents

1. [Basic Queries](#basic-queries)
2. [Filtering & Sorting](#filtering--sorting)
3. [Joins](#joins)
4. [Aggregation](#aggregation)
5. [Subqueries](#subqueries)

---

## 🔍 Basic Queries

### SELECT Statement

```sql
-- Select all columns
SELECT * FROM table_name;

-- Select specific columns
SELECT column1, column2 FROM table_name;

-- Select with alias
SELECT column1 AS alias1, column2 AS alias2 FROM table_name;

-- Select distinct values
SELECT DISTINCT column1 FROM table_name;
```

### WHERE Clause

```sql
-- Basic conditions
SELECT * FROM employees WHERE salary > 50000;
SELECT * FROM employees WHERE department = 'Sales';
SELECT * FROM employees WHERE age BETWEEN 25 AND 35;
SELECT * FROM employees WHERE city IN ('NYC', 'LA', 'Chicago');
SELECT * FROM employees WHERE name LIKE 'J%';
SELECT * FROM employees WHERE manager_id IS NULL;
```

---

## 🔄 Filtering & Sorting

### ORDER BY

```sql
-- Ascending order (default)
SELECT * FROM employees ORDER BY name;

-- Descending order
SELECT * FROM employees ORDER BY salary DESC;

-- Multiple columns
SELECT * FROM employees ORDER BY department, salary DESC;
```

### LIMIT & OFFSET

```sql
-- Top 10 rows
SELECT * FROM employees LIMIT 10;

-- Skip first 10, get next 10
SELECT * FROM employees LIMIT 10 OFFSET 10;

-- Pagination
SELECT * FROM employees LIMIT 10 OFFSET 20;
```

---

## 🔗 Joins

### Types of Joins

| Join Type | Description |
|-----------|-------------|
| **INNER JOIN** | Matching rows in both tables |
| **LEFT JOIN** | All rows in left, matching in right |
| **RIGHT JOIN** | All rows in right, matching in left |
| **FULL OUTER JOIN** | All rows in both tables |
| **CROSS JOIN** | Cartesian product |
| **SELF JOIN** | Table joined with itself |

### Join Examples

```sql
-- INNER JOIN
SELECT e.name, d.department_name
FROM employees e
INNER JOIN departments d ON e.department_id = d.id;

-- LEFT JOIN
SELECT e.name, d.department_name
FROM employees e
LEFT JOIN departments d ON e.department_id = d.id;

-- RIGHT JOIN
SELECT e.name, d.department_name
FROM employees e
RIGHT JOIN departments d ON e.department_id = d.id;

-- FULL OUTER JOIN
SELECT e.name, d.department_name
FROM employees e
FULL OUTER JOIN departments d ON e.department_id = d.id;
```

---

## 📊 Aggregation

### Aggregate Functions

| Function | Description |
|----------|-------------|
| `COUNT()` | Count rows |
| `SUM()` | Sum values |
| `AVG()` | Average value |
| `MIN()` | Minimum value |
| `MAX()` | Maximum value |

### GROUP BY

```sql
-- Count by department
SELECT department, COUNT(*) as employee_count
FROM employees
GROUP BY department;

-- Average salary by department
SELECT department, AVG(salary) as avg_salary
FROM employees
GROUP BY department;

-- HAVING clause
SELECT department, AVG(salary) as avg_salary
FROM employees
GROUP BY department
HAVING AVG(salary) > 60000;
```

---

## 🔍 Subqueries

### Types

```sql
-- WHERE subquery
SELECT * FROM employees
WHERE department_id IN (SELECT id FROM departments WHERE name = 'Sales');

-- FROM subquery
SELECT * FROM (
    SELECT department, AVG(salary) as avg_salary
    FROM employees
    GROUP BY department
) AS dept_avg
WHERE avg_salary > 60000;

-- SELECT subquery
SELECT name, salary,
    (SELECT AVG(salary) FROM employees) as company_avg
FROM employees;
```

---

## 🛠️ Data Manipulation

### INSERT

```sql
-- Single row
INSERT INTO employees (name, department, salary)
VALUES ('John Doe', 'Sales', 55000);

-- Multiple rows
INSERT INTO employees (name, department, salary)
VALUES 
    ('Jane Smith', 'Marketing', 60000),
    ('Bob Johnson', 'IT', 75000);
```

### UPDATE

```sql
-- Update single column
UPDATE employees SET salary = 60000 WHERE name = 'John Doe';

-- Update multiple columns
UPDATE employees 
SET salary = 65000, department = 'Senior Sales'
WHERE name = 'John Doe';
```

### DELETE

```sql
-- Delete specific rows
DELETE FROM employees WHERE name = 'John Doe';

-- Delete all rows
DELETE FROM employees;
```

---

## 🎯 Window Functions

```sql
-- Row number
SELECT name, department, salary,
    ROW_NUMBER() OVER (ORDER BY salary DESC) as rank
FROM employees;

-- Rank with ties
SELECT name, department, salary,
    RANK() OVER (ORDER BY salary DESC) as rank
FROM employees;

-- Dense rank
SELECT name, department, salary,
    DENSE_RANK() OVER (ORDER BY salary DESC) as rank
FROM employees;

-- Partition by
SELECT name, department, salary,
    ROW_NUMBER() OVER (PARTITION BY department ORDER BY salary DESC) as dept_rank
FROM employees;
```

---

## 🔗 Related Resources

| Resource | Link |
|----------|------|
| 🗄️ SQL Tutorial | [ChatWhole.com/sql](https://chatwhole.com/sql) |
| 🐍 Python for SQL | [ChatWhole.com/python](https://chatwhole.com/python) |
| 📊 Data Science | [ChatWhole.com/data-science](https://chatwhole.com/data-science) |

---

<p align="center">
  <a href="https://chatwhole.com">← Back to ChatWhole.com</a>
</p>
