SQL INTERVIEW QUESTIONS – DAY 8

36. What is the difference between UNION and UNION ALL in SQL?

Answer:
UNION combines the results of two or more SELECT queries and removes duplicate rows. UNION ALL combines the results and keeps duplicate rows.

Example:
SELECT city FROM customers
UNION
SELECT city FROM suppliers;

UNION ALL example:
SELECT city FROM customers
UNION ALL
SELECT city FROM suppliers;


37. What is a Subquery in SQL?

Answer:
A subquery is a query written inside another SQL query. It is used to provide a result that can be used by the outer query.

Example:
SELECT name, salary
FROM employees
WHERE salary > (
    SELECT AVG(salary)
    FROM employees
);


38. What is the NOT NULL constraint in SQL?

Answer:
The NOT NULL constraint ensures that a column cannot contain NULL values. It is used when a value is required for every row.

Example:
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    name VARCHAR(50) NOT NULL
);


39. What is the ORDER BY clause used for in SQL?

Answer:
The ORDER BY clause is used to sort the result of a query in ascending or descending order. ASC is the default order, while DESC sorts in descending order.

Example:
SELECT name, salary
FROM employees
ORDER BY salary DESC;


40. What is normalization in SQL?

Answer:
Normalization is the process of organizing data in database tables to reduce data redundancy and improve data consistency. It usually involves dividing large tables into smaller related tables.

Example:
Instead of storing department details repeatedly in an Employees table, we can create a separate Departments table and connect it using a department_id.




