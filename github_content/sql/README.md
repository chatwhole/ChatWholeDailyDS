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

## 🎓 Full Course Lesson Index

Follow the complete **70-lesson SQL course** on [ChatWhole.com](https://chatwhole.com/learn/sql/) - every lesson linked below.

### Part 1: Lessons 01-25

| # | Lesson |
|---|--------|
| 01 | [Sql Introduction](https://chatwhole.com/learn/sql/01-sql-introduction/) |
| 02 | [Database Concepts](https://chatwhole.com/learn/sql/02-database-concepts/) |
| 03 | [Sql Data Types](https://chatwhole.com/learn/sql/03-sql-data-types/) |
| 04 | [Create Table](https://chatwhole.com/learn/sql/04-create-table/) |
| 05 | [Insert Data](https://chatwhole.com/learn/sql/05-insert-data/) |
| 06 | [Select Basics](https://chatwhole.com/learn/sql/06-select-basics/) |
| 07 | [Where Clause](https://chatwhole.com/learn/sql/07-where-clause/) |
| 08 | [Distinct](https://chatwhole.com/learn/sql/08-distinct/) |
| 09 | [Order By](https://chatwhole.com/learn/sql/09-order-by/) |
| 10 | [Limit Offset](https://chatwhole.com/learn/sql/10-limit-offset/) |
| 11 | [Aliases](https://chatwhole.com/learn/sql/11-aliases/) |
| 12 | [Update Data](https://chatwhole.com/learn/sql/12-update-data/) |
| 13 | [Delete Data](https://chatwhole.com/learn/sql/13-delete-data/) |
| 14 | [And Or Not](https://chatwhole.com/learn/sql/14-and-or-not/) |
| 15 | [In Between](https://chatwhole.com/learn/sql/15-in-between/) |
| 16 | [Like Wildcards](https://chatwhole.com/learn/sql/16-like-wildcards/) |
| 17 | [Is Null](https://chatwhole.com/learn/sql/17-is-null/) |
| 18 | [Inner Join](https://chatwhole.com/learn/sql/18-inner-join/) |
| 19 | [Left Join](https://chatwhole.com/learn/sql/19-left-join/) |
| 20 | [Right Join](https://chatwhole.com/learn/sql/20-right-join/) |
| 21 | [Full Join](https://chatwhole.com/learn/sql/21-full-join/) |
| 22 | [Cross Join](https://chatwhole.com/learn/sql/22-cross-join/) |
| 23 | [Self Join](https://chatwhole.com/learn/sql/23-self-join/) |
| 24 | [Union Intersect Except](https://chatwhole.com/learn/sql/24-union-intersect-except/) |
| 25 | [Group By](https://chatwhole.com/learn/sql/25-group-by/) |

### Part 2: Lessons 26-50

| # | Lesson |
|---|--------|
| 26 | [Having](https://chatwhole.com/learn/sql/26-having/) |
| 27 | [Aggregate Functions Overview](https://chatwhole.com/learn/sql/27-aggregate-functions-overview/) |
| 28 | [Count Sum Avg](https://chatwhole.com/learn/sql/28-count-sum-avg/) |
| 29 | [Min Max](https://chatwhole.com/learn/sql/29-min-max/) |
| 30 | [String Functions](https://chatwhole.com/learn/sql/30-string-functions/) |
| 31 | [Date Time Functions](https://chatwhole.com/learn/sql/31-date-time-functions/) |
| 32 | [Numeric Functions](https://chatwhole.com/learn/sql/32-numeric-functions/) |
| 33 | [Subqueries](https://chatwhole.com/learn/sql/33-subqueries/) |
| 34 | [Correlated Subqueries](https://chatwhole.com/learn/sql/34-correlated-subqueries/) |
| 35 | [Case Expression](https://chatwhole.com/learn/sql/35-case-expression/) |
| 36 | [Coalesce Nullif](https://chatwhole.com/learn/sql/36-coalesce-nullif/) |
| 37 | [Views](https://chatwhole.com/learn/sql/37-views/) |
| 38 | [Indexes](https://chatwhole.com/learn/sql/38-indexes/) |
| 39 | [Constraints](https://chatwhole.com/learn/sql/39-constraints/) |
| 40 | [Alter Table](https://chatwhole.com/learn/sql/40-alter-table/) |
| 41 | [Drop Table Truncate](https://chatwhole.com/learn/sql/41-drop-table-truncate/) |
| 42 | [Transactions](https://chatwhole.com/learn/sql/42-transactions/) |
| 43 | [Stored Procedures](https://chatwhole.com/learn/sql/43-stored-procedures/) |
| 44 | [User Defined Functions](https://chatwhole.com/learn/sql/44-user-defined-functions/) |
| 45 | [Triggers](https://chatwhole.com/learn/sql/45-triggers/) |
| 46 | [Window Functions Intro](https://chatwhole.com/learn/sql/46-window-functions-intro/) |
| 47 | [Row Number Rank Dense Rank](https://chatwhole.com/learn/sql/47-row-number-rank-dense-rank/) |
| 48 | [Lead Lag](https://chatwhole.com/learn/sql/48-lead-lag/) |
| 49 | [Cte Intro](https://chatwhole.com/learn/sql/49-cte-intro/) |
| 50 | [Recursive Cte](https://chatwhole.com/learn/sql/50-recursive-cte/) |

### Part 3: Lessons 51-70

| # | Lesson |
|---|--------|
| 51 | [Normalization](https://chatwhole.com/learn/sql/51-normalization/) |
| 52 | [Er Diagrams](https://chatwhole.com/learn/sql/52-er-diagrams/) |
| 53 | [Query Performance](https://chatwhole.com/learn/sql/53-query-performance/) |
| 54 | [Explain Analyze](https://chatwhole.com/learn/sql/54-explain-analyze/) |
| 55 | [Sql Best Practices](https://chatwhole.com/learn/sql/55-sql-best-practices/) |
| 56 | [Sql Joins Masterclass](https://chatwhole.com/learn/sql/56-sql-joins-masterclass/) |
| 57 | [Practicing Sql](https://chatwhole.com/learn/sql/57-practicing-sql/) |
| 58 | [Sql Glossary](https://chatwhole.com/learn/sql/58-sql-glossary/) |
| 59 | [Sql Cheatsheet](https://chatwhole.com/learn/sql/59-sql-cheatsheet/) |
| 60 | [Window Functions Advanced](https://chatwhole.com/learn/sql/60-window-functions-advanced/) |
| 61 | [Pivot Unpivot](https://chatwhole.com/learn/sql/61-pivot-unpivot/) |
| 62 | [Json In Sql](https://chatwhole.com/learn/sql/62-json-in-sql/) |
| 63 | [Full Text Search](https://chatwhole.com/learn/sql/63-full-text-search/) |
| 64 | [Postgresql Vs Mysql](https://chatwhole.com/learn/sql/64-postgresql-vs-mysql/) |
| 65 | [Sql For Data Analysis](https://chatwhole.com/learn/sql/65-sql-for-data-analysis/) |
| 66 | [Cte Deep Dive](https://chatwhole.com/learn/sql/66-cte-deep-dive/) |
| 67 | [Table Partitioning](https://chatwhole.com/learn/sql/67-table-partitioning/) |
| 68 | [Sql Etl Pipelines](https://chatwhole.com/learn/sql/68-sql-etl-pipelines/) |
| 69 | [Sql Security](https://chatwhole.com/learn/sql/69-sql-security/) |
| 70 | [Sql A To Z](https://chatwhole.com/learn/sql/70-sql-a-to-z/) |

---

## 🔗 Related Resources

| Resource | Link |
|----------|------|
| 🗄️ SQL Tutorial | [ChatWhole.com/sql](https://chatwhole.com/sql) |
| 🐍 Python for SQL | [ChatWhole.com/python](https://chatwhole.com/python) |
| 📊 Data Science | [ChatWhole.com/data-science](https://chatwhole.com/data-science) |
| 🤖 ML: Feature Stores | [ChatWhole.com/learn/machine-learning/46-feature-stores](https://chatwhole.com/learn/machine-learning/46-feature-stores/) |
| 🤖 ML: ML System Design | [ChatWhole.com/learn/machine-learning/45-ml-system-design](https://chatwhole.com/learn/machine-learning/45-ml-system-design/) |
| 📡 Kafka: Schema Registry | [ChatWhole.com/learn/kafka/05-schema-registry](https://chatwhole.com/learn/kafka/05-schema-registry/) |
| 📡 Kafka: Connect Deep Dive | [ChatWhole.com/learn/kafka/09-kafka-connect-deep-dive](https://chatwhole.com/learn/kafka/09-kafka-connect-deep-dive/) |

---

<p align="center">
  <a href="https://chatwhole.com">← Back to ChatWhole.com</a>
</p>
