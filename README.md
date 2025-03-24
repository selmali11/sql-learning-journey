## SQL Learning Exercises

This repo documents my journey to learn SQL from beginner to advanced utilizing an internal LLM solution as a tool to facilitate the learning process.

## Outline

1. [Concept 1: SELECT Statement](#concept-1-select-statement)
2. [Concept 2: WHERE Clause](#concept-2-where-clause)
3. [Concept 3: ORDER BY Clause](#concept-3-order-by-clause)
4. [Concept 4: INSERT INTO Statement](#concept-4-insert-into-statement)
5. [Concept 5: UPDATE Statement](#concept-5-update-statement)
6. [Concept 6: DELETE Statement](#concept-6-delete-statement)
7. [Concept 7: INNER JOIN](#concept-7-inner-join)
8. [Concept 8: LEFT JOIN](#concept-8-left-join)
9. [Concept 9: GROUP BY Clause](#concept-9-group-by-clause)
10. [Concept 10: HAVING Clause](#concept-10-having-clause)
11. [Concept 11: UNION Operator](#concept-11-union-operator)
12. [Concept 12: Subqueries](#concept-12-subqueries)
13. [Concept 13: Aggregate Functions](#concept-13-aggregate-functions)
14. [Concept 14: DISTINCT Keyword](#concept-14-distinct-keyword)
15. [Concept 15: SQL Constraints](#concept-15-sql-constraints)
16. [Concept 16: SQL Functions](#concept-16-sql-functions)
17. [Concept 17: SQL Views](#concept-17-sql-views)
18. [Concept 18: Indexes](#concept-18-indexes)
19. [Concept 19: Stored Procedures](#concept-19-stored-procedures)
20. [Concept 20: Window Functions](#concept-20-window-functions)
21. [Concept 21: Common Table Expressions (CTEs)](#concept-21-common-table-expressions-ctes)

## Concepts Covered

### Concept 1: SELECT Statement

**Overview**:  
The SELECT statement is used to select data from a database. The data returned is stored in a result table, sometimes called the result-set.

**Syntax**:
```sql
SELECT column1, column2, ...
FROM table_name;
```

To select all columns from a table, you can use the asterisk (*) symbol:
```sql
SELECT * FROM table_name;
```

**Practice Question**:  
What is the syntax for selecting all columns from a table named 'employees'?

**User's Answer**:
```sql
select * from employees;
```

**Provided Answer**:
```sql
SELECT * FROM employees;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 2: WHERE Clause

**Overview**:  
The WHERE clause is used to filter records. It is used to extract only those records that fulfill a specified condition.

**Syntax**:
```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

**Practice Question**:  
Write a SQL query to select all columns from a table named 'employees' where the 'department' is 'Sales'.

**User's Answer**:
```sql
select * from employees where department = 'Sales';
```

**Provided Answer**:
```sql
SELECT * FROM employees WHERE department = 'Sales';
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 3: ORDER BY Clause

**Overview**:  
The ORDER BY clause is used to sort the result-set in ascending or descending order. By default, it sorts the records in ascending order.

**Syntax**:
```sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```

**Practice Question**:  
Write a SQL query to select all columns from a table named 'employees' and sort the result by 'salary' in descending order.

**User's Answer**:
```sql
select * from employees order by salary desc;
```

**Provided Answer**:
```sql
SELECT * FROM employees ORDER BY salary DESC;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 4: INSERT INTO Statement

**Overview**:  
The INSERT INTO statement is used to insert new records in a table.

**Syntax**:
```sql
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

If you are adding values for all the columns of the table, you do not need to specify the column names in the SQL query:
```sql
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
```

**Practice Question**:  
Write a SQL query to insert a new record into the 'employees' table with the following details:
- Name: 'John Doe'
- Department: 'HR'
- Salary: 50000

**User's Answer**:
```sql
insert into employees (name, department, salary) values ('John Doe', 'HR', 50000);
```

**Provided Answer**:
```sql
INSERT INTO employees (name, department, salary) VALUES ('John Doe', 'HR', 50000);
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 5: UPDATE Statement

**Overview**:  
The UPDATE statement is used to modify the existing records in a table.

**Syntax**:
```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

**Practice Question**:  
Write a SQL query to update the salary of 'John Doe' in the 'employees' table to 55000.

**User's Answer**:
```sql
update employees set salary = 55000 where name = 'John Doe';
```

**Provided Answer**:
```sql
UPDATE employees SET salary = 55000 WHERE name = 'John Doe';
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 6: DELETE Statement

**Overview**:  
The DELETE statement is used to delete existing records in a table.

**Syntax**:
```sql
DELETE FROM table_name
WHERE condition;
```

**Practice Question**:  
Write a SQL query to delete the record of 'John Doe' from the 'employees' table.

**User's Answer**:
```sql
delete from employees where name = 'John Doe';
```

**Provided Answer**:
```sql
DELETE FROM employees WHERE name = 'John Doe';
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 7: INNER JOIN

**Overview**:  
The INNER JOIN keyword selects records that have matching values in both tables.

**Syntax**:
```sql
SELECT column1, column2, ...
FROM table1
INNER JOIN table2
ON table1.common_column = table2.common_column;
```

**Practice Question**:  
Write a SQL query to select all columns from two tables, 'employees' and 'departments', where the 'department_id' in 'employees' matches the 'id' in 'departments'.

**User's Answer**:
```sql
select * from employees inner join departments on employees.department_id = departments.id;
```

**Provided Answer**:
```sql
SELECT * FROM employees INNER JOIN departments ON employees.department_id = departments.id;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 8: LEFT JOIN

**Overview**:  
The LEFT JOIN keyword returns all records from the left table (table1), and the matched records from the right table (table2). The result is NULL from the right side if there is no match.

**Syntax**:
```sql
SELECT column1, column2, ...
FROM table1
LEFT JOIN table2
ON table1.common_column = table2.common_column;
```

**Practice Question**:  
Write a SQL query to select all columns from two tables, 'employees' and 'departments', where the 'department_id' in 'employees' matches the 'id' in 'departments', and include all employees even if they do not belong to a department.

**User's Answer**:
```sql
SELECT * FROM employees LEFT JOIN departments ON employees.department_id = departments.id;
```

**Provided Answer**:
```sql
SELECT * FROM employees LEFT JOIN departments ON employees.department_id = departments.id;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 9: GROUP BY Clause

**Overview**:  
The GROUP BY statement is used to group the result-set by one or more columns. It is often used with aggregate functions (COUNT, MAX, MIN, SUM, AVG) to group the result-set by one or more columns.

**Syntax**:
```sql
SELECT column1, aggregate_function(column2)
FROM table_name
WHERE condition
GROUP BY column1, column2, ...;
```

**Practice Question**:  
Write a SQL query to count the number of employees in each department from the 'employees' table.

**User's Answer**:
```sql
select department_id, count(*) as total_employees from employees group by department_id;
```

**Provided Answer**:
```sql
SELECT department_id, COUNT(*) AS total_employees FROM employees GROUP BY department_id;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 10: HAVING Clause

**Overview**:  
The HAVING clause was added to SQL because the WHERE keyword cannot be used with aggregate functions. The HAVING clause is used to filter records that work on summarized GROUP BY results.

**Syntax**:
```sql
SELECT column1, aggregate_function(column2)
FROM table_name
WHERE condition
GROUP BY column1, column2, ...
HAVING condition;
```

**Practice Question**:  
Write a SQL query to count the number of employees in each department from the 'employees' table, but only include departments with more than 5 employees.

**User's Answer**:
```sql
select department_id, count(*) as total_employees from employees group by department_id having count(*) > 5;
```

**Provided Answer**:
```sql
SELECT department_id, COUNT(*) AS total_employees FROM employees GROUP BY department_id HAVING COUNT(*) > 5;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 11: UNION Operator

**Overview**:  
The UNION operator is used to combine the result-set of two or more SELECT statements. Each SELECT statement within the UNION must have the same number of columns in the result sets with similar data types. The columns in each SELECT statement must also be in the same order.

**Syntax**:
```sql
SELECT column1, column2, ...
FROM table1
UNION
SELECT column1, column2, ...
FROM table2;
```

**Practice Question**:  
Write a SQL query to combine the results of two tables, 'employees_2020' and 'employees_2021', selecting all columns from both tables.

**User's Answer**:
```sql
select * from employees_2020 union select * from employees_2021;
```

**Provided Answer**:
```sql
SELECT * FROM employees_2020 UNION SELECT * FROM employees_2021;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 12: Subqueries

**Overview**:  
A subquery is a SQL query nested inside a larger query. Subqueries can be used in SELECT, INSERT, UPDATE, and DELETE statements, as well as in other subqueries. A subquery is usually added within the WHERE clause of another SQL SELECT statement.

**Syntax**:
```sql
SELECT column1, column2, ...
FROM table_name
WHERE column_name OPERATOR (SELECT column_name FROM table_name WHERE condition);
```

**Practice Question**:  
Write a SQL query to select all columns from the 'employees' table where the 'department_id' matches any 'id' in the 'departments' table.

**User's Answer**:
```sql
select * from employees where department_id in (select id from departments);
```

**Provided Answer**:
```sql
SELECT * FROM employees WHERE department_id IN (SELECT id FROM departments);
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 13: Aggregate Functions

**Overview**:  
Aggregate functions perform a calculation on a set of values and return a single value. The following are commonly used aggregate functions:
- `COUNT()`: Returns the number of rows.
- `SUM()`: Returns the sum of a numeric column.
- `AVG()`: Returns the average value of a numeric column.
- `MIN()`: Returns the smallest value.
- `MAX()`: Returns the largest value.

**Syntax**:
```sql
SELECT aggregate_function(column)
FROM table_name
WHERE condition;
```

**Practice Question**:  
Write a SQL query to find the average salary of all employees from the 'employees' table.

**User's Answer**:
```sql
select avg(salary) as avg_salary from employees;
```

**Provided Answer**:
```sql
SELECT AVG(salary) AS avg_salary FROM employees;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 14: DISTINCT Keyword

**Overview**:  
The DISTINCT keyword is used in SQL to return only distinct (different) values. It can be used to remove duplicates from the result set.

**Syntax**:
```sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
```

**Practice Question**:  
Write a SQL query to select distinct department IDs from the 'employees' table.

**User's Answer**:
```sql
select distinct department_id from employees;
```

**Provided Answer**:
```sql
SELECT DISTINCT department_id FROM employees;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 15: SQL Constraints

**Overview**:  
SQL constraints are used to specify rules for the data in a table. Constraints can be specified when the table is created with the CREATE TABLE statement, or after the table is created with the ALTER TABLE statement. Common constraints include:
- `NOT NULL`: Ensures that a column cannot have a NULL value.
- `UNIQUE`: Ensures that all values in a column are different.
- `PRIMARY KEY`: A combination of a NOT NULL and UNIQUE. Uniquely identifies each row in a table.
- `FOREIGN KEY`: Prevents actions that would destroy links between tables.
- `CHECK`: Ensures that the values in a column satisfy a specific condition.
- `DEFAULT`: Sets a default value for a column if no value is specified.

**Syntax**:
```sql
CREATE TABLE table_name (
    column1 datatype constraint,
    column2 datatype constraint,
    ...
);
```

**Practice Question**:  
Write a SQL query to create a table named 'departments' with the following columns:
- `id` (integer, primary key)
- `name` (varchar, not null, unique)

**User's Answer**:
```sql
create table departments (
id integer primary key,
name varchar not null unique);
```

**Provided Answer**:
```sql
CREATE TABLE departments (
    id INTEGER PRIMARY KEY,
    name VARCHAR NOT NULL UNIQUE
);
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 16: SQL Functions

**Overview**:  
SQL functions are built-in functions that perform operations on data. There are various types of functions, including:
- Aggregate functions: `COUNT()`, `SUM()`, `AVG()`, `MIN()`, `MAX()`
- String functions: `LENGTH()`, `UPPER()`, `LOWER()`, `SUBSTRING()`
- Date functions: `NOW()`, `CURDATE()`, `DATE_ADD()`, `DATE_SUB()`

**Syntax**:
```sql
SELECT function_name(column)
FROM table_name
WHERE condition;
```

**Practice Question**:  
Write a SQL query to get the current date and time.

**User's Answer**:
```sql
select now();
```

**Provided Answer**:
```sql
SELECT NOW();
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 17: SQL Views

**Overview**:  
A view is a virtual table based on the result set of an SQL statement. A view contains rows and columns, just like a real table. The fields in a view are fields from one or more real tables in the database. You can add SQL functions, WHERE, and JOIN statements to a view and present the data as if the data were coming from a single table.

**Syntax**:
```sql
CREATE VIEW view_name AS
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

**Practice Question**:  
Write a SQL query to create a view named 'employee_view' that includes the 'name' and 'salary' columns from the 'employees' table.

**User's Answer**:
```sql
create view employee_view as select name, salary from employees;
```

**Provided Answer**:
```sql
CREATE VIEW employee_view AS
SELECT name, salary FROM employees;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 18: Indexes

**Overview**:  
Indexes are used to retrieve data from the database more quickly than otherwise. The users cannot see the indexes; they are just used to speed up searches/queries. Updating a table with indexes takes more time than updating a table without (due to the re-indexing), so index creation should be considered based on the frequency of reads vs. writes.

**Syntax**:
```sql
CREATE INDEX index_name
ON table_name (column1, column2, ...);
```

To create a unique index:
```sql
CREATE UNIQUE INDEX index_name
ON table_name (column1, column2, ...);
```

**Practice Question**:  
Write a SQL query to create an index named 'idx_department' on the 'department_id' column of the 'employees' table.

**User's Answer**:
```sql
create index idx_department on employees(department_id);
```

**Provided Answer**:
```sql
CREATE INDEX idx_department ON employees(department_id);
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 19: Stored Procedures

**Overview**:  
A stored procedure is a prepared SQL code that you can save and reuse. So if you have a SQL query that you write over and over again, save it as a stored procedure, and then call it to execute it.

**Syntax**:
```sql
CREATE PROCEDURE procedure_name
AS
BEGIN
    -- SQL statements
END;

-- Execute the stored procedure
EXEC procedure_name;
```

**Practice Question**:  
Write a SQL stored procedure named 'GetEmployeeDetails' that selects the 'name' and 'salary' columns from the 'employees' table.

**User's Answer**:
```sql
create procedure GetEmployeeDetails 
as 
begin
select name, salary from employees
end

exec GetEmployeeDetails;
```

**Provided Answer**:
```sql
CREATE PROCEDURE GetEmployeeDetails 
AS 
BEGIN
    SELECT name, salary FROM employees;
END;

EXEC GetEmployeeDetails;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 20: Window Functions

**Overview**:  
Window functions perform a calculation across a set of table rows that are somehow related to the current row. They are often used to perform aggregations and calculations on a subset of rows that are related to the current row based on some criteria.

**Syntax**:
```sql
SELECT column1, column2, 
       window_function() OVER (PARTITION BY column1 ORDER BY column2)
FROM table_name;
```

**Common Window Functions**:
- `ROW_NUMBER()`: Assigns a unique number to each row within the partition of a result set.
- `RANK()`: Assigns a rank to each row within the partition of a result set.
- `DENSE_RANK()`: Similar to `RANK()`, but without gaps in ranking values.
- `SUM()`, `AVG()`, `MIN()`, `MAX()`: Aggregate functions that can be used as window functions.

### Window Function 1: ROW_NUMBER()

**Practice Question**:  
Write a SQL query using the `ROW_NUMBER()` window function to assign a unique row number to each employee in the 'employees' table, partitioned by 'department_id' and ordered by 'salary' in descending order.

**User's Answer**:
```sql
select employee_id, row_number() over (partition by department_id order by salary desc) from employees;
```

**Provided Answer**:
```sql
SELECT employee_id, 
       ROW_NUMBER() OVER (PARTITION BY department_id ORDER BY salary DESC) AS row_num
FROM employees;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Window Function 2: RANK()

**Overview**:  
The `RANK()` function assigns a rank to each row within the partition of a result set. If two rows have the same rank, the next rank will be the rank number plus the number of rows with the same rank.

**Syntax**:
```sql
RANK() OVER (PARTITION BY column1 ORDER BY column2)
```

**Practice Question**:  
Write a SQL query using the `RANK()` window function to assign a rank to each employee in the 'employees' table, partitioned by 'department_id' and ordered by 'salary' in descending order.

**User's Answer**:
```sql
select employee_id, rank() over (partition by department_id order by salary desc) as rank from employees;
```

**Provided Answer**:
```sql
SELECT employee_id, 
       RANK() OVER (PARTITION BY department_id ORDER BY salary DESC) AS rank
FROM employees;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Window Function 3: DENSE_RANK()

**Overview**:  
The `DENSE_RANK()` function is similar to the `RANK()` function, but it does not skip ranks when there are ties. If two rows have the same rank, the next rank will be the rank number plus one.

**Syntax**:
```sql
DENSE_RANK() OVER (PARTITION BY column1 ORDER BY column2)
```

**Practice Question**:  
Write a SQL query using the `DENSE_RANK()` window function to assign a dense rank to each employee in the 'employees' table, partitioned by 'department_id' and ordered by 'salary' in descending order.

**User's Answer**:
```sql
SELECT employee_id, 
       DENSE_RANK() OVER (PARTITION BY department_id ORDER BY salary DESC) AS rank
FROM employees;
```

**Provided Answer**:
```sql
SELECT employee_id, 
       DENSE_RANK() OVER (PARTITION BY department_id ORDER BY salary DESC) AS rank
FROM employees;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Window Function 4: SUM()

**Overview**:  
The `SUM()` window function calculates the cumulative sum of a set of values within a partition.

**Syntax**:
```sql
SUM(column) OVER (PARTITION BY column1 ORDER BY column2)
```

**Practice Question**:  
Write a SQL query using the `SUM()` window function to calculate the cumulative salary for each employee in the 'employees' table, partitioned by 'department_id' and ordered by 'employee_id'.

**User's Answer**:
```sql
SELECT employee_id, 
       SUM(salary) OVER (PARTITION BY department_id ORDER BY employee_id) AS total_salary
FROM employees;
```

**Provided Answer**:
```sql
SELECT employee_id, 
       SUM(salary) OVER (PARTITION BY department_id ORDER BY employee_id) AS total_salary
FROM employees;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

### Concept 21: Common Table Expressions (CTEs)

**Overview**:  
A Common Table Expression (CTE) is a temporary result set that you can reference within a `SELECT`, `INSERT`, `UPDATE`, or `DELETE` statement. CTEs can be used to simplify complex joins and subqueries, and they can be recursive.

**Syntax**:
```sql
WITH cte_name AS (
    -- SQL query
)
SELECT column1, column2, ...
FROM cte_name;
```

**Example**:
```sql
WITH EmployeeCTE AS (
    SELECT employee_id, department_id, salary
    FROM employees
)
SELECT department_id, AVG(salary) AS avg_salary
FROM EmployeeCTE
GROUP BY department_id;
```

**Practice Question**:  
Write a SQL query using a CTE to select the 'employee_id', 'department_id', and 'salary' columns from the 'employees' table, and then use the CTE to find the total salary by 'department_id'.

**User's Answer**:
```sql
WITH EmployeeCTE AS (
    SELECT employee_id, department_id, salary
    FROM employees
)
SELECT department_id, SUM(salary)
FROM EmployeeCTE
GROUP BY department_id;
```

**Provided Answer**:
```sql
WITH EmployeeCTE AS (
    SELECT employee_id, department_id, salary
    FROM employees
)
SELECT department_id, SUM(salary) AS total_salary
FROM EmployeeCTE
GROUP BY department_id;
```

Validity of User's Answer:

✅ Correct
☐ Not Correct
☐ Almost Correct

---

## User Inquiries

### Concept 18: Indexes

**User Inquiry**: Can you explain a little bit more how indexes work? Are indexes similar to hash tables?

**Response to Inquiry**:

**Indexes** in databases are used to speed up the retrieval of rows by using a data structure that allows for quick lookups. Here's a simple breakdown:

- **Purpose**: To improve the speed of data retrieval operations on a database table at the cost of additional writes and storage space.
- **Structure**: Indexes can be implemented using various data structures, including B-trees, hash tables, and others. The most common type of index in many databases is the B-tree index.
- **Usage**: When a query searches for a specific value, the index allows the database to find the location of the data quickly without scanning the entire table.

**Hash tables** are a different type of data structure:

- **Purpose**: To provide very fast access to data, typically in constant time \(O(1)\), for operations such as lookups, insertions, and deletions.
- **Structure**: A hash table uses a hash function to compute an index into an array of buckets or slots, from which the desired value can be found.
- **Usage**: Hash tables are often used in situations where fast access to data is crucial, such as in caching mechanisms or implementing associative arrays.

**Comparison**:

- **Speed**: Both indexes and hash tables aim to speed up data access, but they do so in different ways. Hash tables generally offer constant time complexity \(O(1)\), while indexes like B-trees offer logarithmic time complexity \(O(\log n)\).
- **Complexity**: Indexes, especially B-trees, can handle range queries efficiently, whereas hash tables are typically better suited for exact-match queries.
- **Storage**: Creating an index in a database incurs additional storage overhead, similar to hash tables, which require extra space for the array and hash function.

**Example**:

**Index Example**:
```sql
CREATE INDEX idx_name ON employees(name);
```
This creates an index on the `name` column of the `employees` table, allowing for faster searches by name.

**Hash Table Example** (in Python):
```python
hash_table = {}
hash_table["name"] = "John Doe"
print(hash_table["name"])  # Output: John Doe
```
This creates a hash table with a key-value pair, allowing for fast retrieval of the value by the key.

In summary, while both indexes and hash tables aim to improve data retrieval times, they are used in different contexts and have distinct characteristics.

---

### Concept 18: Indexes

**User Inquiry**: Why use a unique index? In what situations do we opt for a unique index vs a regular index?

**Response to Inquiry**:

**Unique Indexes** and regular indexes serve different purposes in a database. Here's a detailed explanation of why and when to use each:

**Unique Index**:

**Purpose**:
- Ensures that all values in the indexed column(s) are unique.
- Prevents duplicate values in the column(s), thereby enforcing data integrity.

**Usage**:
- Use a unique index when you need to ensure that no duplicate values are allowed in a column.
- Commonly used for columns that require uniqueness, such as email addresses, usernames, or any other field that should have unique values.

**Example**:
- Email addresses in a user table should be unique to prevent multiple accounts with the same email.

**Syntax**:
```sql
CREATE UNIQUE INDEX index_name
ON table_name (column1, column2, ...);
```

**Example**:
```sql
CREATE UNIQUE INDEX idx_email ON users(email);
```

**Regular Index**:

**Purpose**:
- Improves the speed of data retrieval operations.
- Does not enforce uniqueness; allows duplicate values in the indexed column(s).

**Usage**:
- Use a regular index to speed up queries on columns that do not require uniqueness.
- Commonly used for columns that are frequently searched, filtered, or used in JOIN operations.

**Example**:
- Indexing a 'department_id' column in an 'employees' table to speed up queries that filter by department.

**Syntax**:
```sql
CREATE INDEX index_name
ON table_name (column1, column2, ...);
```

**Example**:
```sql
CREATE INDEX idx_department ON employees(department_id);
```

### When to Use Each:

1. **Unique Index**:
   - Use when you need to enforce uniqueness in a column.
   - Examples: email addresses, usernames, social security numbers.

2. **Regular Index**:
   - Use when you need to speed up data retrieval without enforcing uniqueness.
   - Examples: foreign keys, columns frequently used in WHERE clauses, columns used in JOIN operations.

**Summary**:
- **Unique Index**: Ensures data integrity by preventing duplicates.
- **Regular Index**: Speeds up query performance without enforcing uniqueness.

---

### Concept 17: SQL Views

**User Inquiry**: If I were to query a view, does the underlying query that was used to create the view run when I'm querying the view?

**Response to Inquiry**:

Yes, when you query a view, the underlying query that was used to create the view runs to fetch the data. Here's an explanation:

**How Views Work**:

1. **Definition**:
   - A view is defined by a SQL query that selects data from one or more tables. The view itself does not store data; it stores the query definition.

2. **Query Execution**:
   - When you query a view, the database engine replaces the view with its underlying query. Essentially, it runs the original query that defines the view to retrieve the data.
   - Example:
     ```sql
     CREATE VIEW employee_view AS
     SELECT name, salary FROM employees;
     ```
     Querying the view:
     ```sql
     SELECT * FROM employee_view;
     ```
     Internally, this is equivalent to:
     ```sql
     SELECT name, salary FROM employees;
     ```

3. **Dynamic Data Retrieval**:
   - Since the view does not store data, it always reflects the current state of the underlying tables. Any changes (inserts, updates, deletes) in the base tables are immediately visible through the view.
   - Example: If a new employee is added to the `employees` table, querying the `employee_view` will include the new employee's data.

**Materialized Views**:

1. **Definition**:
   - Unlike regular views, materialized views store the result set of the query. They are essentially a snapshot of the data at a specific point in time.

2. **Query Execution**:
   - When you query a materialized view, it retrieves data from the stored result set rather than rerunning the underlying query.
   - Example:
     ```sql
     CREATE MATERIALIZED VIEW employee_mview AS
     SELECT name, salary FROM employees;
     ```

3. **Data Refresh**:
   - Materialized views need to be refreshed to reflect changes in the underlying tables. This can be done manually or automatically based on a schedule.
   - Example: After adding a new employee to the `employees` table, the materialized view will show the new data only after it is refreshed.

---

### Concept 16: SQL Functions

**User Inquiry**: What's the difference between `NOW()` and `CURDATE()`?

**Response to Inquiry**:

**`NOW()`** and **`CURDATE()`** are both date functions in SQL, but they serve different purposes and return different types of information.

**`NOW()`**:
- **Overview**: The `NOW()` function returns the current date and time.
- **Output**: It includes both the date and the time in the format `YYYY-MM-DD HH:MM:SS`.
- **Example**:
  ```sql
  SELECT NOW();
  ```
  **Result**:
  ```
  2023-10-31 14:35:22
  ```

**`CURDATE()`**:
- **Overview**: The `CURDATE()` function returns the current date only.
- **Output**: It includes only the date in the format `YYYY-MM-DD`.
- **Example**:
  ```sql
  SELECT CURDATE();
  ```
  **Result**:
  ```
  2023-10-31
  ```

### Example Usage:

**Using `NOW()`**:
```sql
SELECT NOW();
```
**Result**:
```
2023-10-31 14:35:22
```

**Using `CURDATE()`**:
```sql
SELECT CURDATE();
```
**Result**:
```
2023-10-31
```

---

## Remaining Concepts to Cover

1. **Transactions**
   - Overview
   - Syntax
   - Practice Question

2. **Triggers**
   - Overview
   - Syntax
   - Practice Question

3. **User-Defined Functions**
   - Overview
   - Syntax
   - Practice Question

4. **Advanced Joins**
   - CROSS JOIN
     - Overview
     - Syntax
     - Practice Question
   - SELF JOIN
     - Overview
     - Syntax
     - Practice Question

5. **Pivot Tables**
   - Overview
   - Syntax
   - Practice Question

6. **Temporary Tables**
   - Overview
   - Syntax
   - Practice Question

7. **Data Types**
   - Overview
   - Practice Question

8. **Advanced Query Techniques**
   - EXISTS and NOT EXISTS
     - Overview
     - Syntax
     - Practice Question
   - CASE Statements
     - Overview
     - Syntax
     - Practice Question
   - COALESCE and NULLIF
     - Overview
     - Syntax
     - Practice Question

9. **Performance Tuning**
   - Overview
   - Practice Question

10. **Database Design**
    - Normalization and Denormalization
      - Overview
      - Practice Question
    - Keys (Primary, Foreign, Composite)
      - Overview
      - Practice Question

11. **Security**
    - GRANT and REVOKE Privileges
      - Overview
      - Syntax
      - Practice Question
    - Roles and Permissions
      - Overview
      - Practice Question
    - Data Encryption
      - Overview
      - Practice Question

12. **Backup and Restore**
    - Overview
    - Practice Question

13. **JSON and XML Data**
    - Storing and Querying JSON and XML Data
      - Overview
      - Syntax
      - Practice Question

14. **Case Studies and Real-World Scenarios**
    - Practical Applications
    - Complex Query Examples

---
