# 🔹 RETRIEVING DATA – SET 3 (EMPLOYEE TABLE – AGGREGATE & STRING FUNCTIONS)

---

## 1. Display the total number of employees working in the company

📌 Using `COUNT(*)`

```sql
SELECT COUNT(*) AS total_employees
FROM employee;
```

---

## 2. Display the total salary being paid to all employees

📌 Using `SUM(sal)`

```sql
SELECT SUM(sal) AS total_salary
FROM employee;
```

---

## 3. Display the maximum salary from employee table

📌 Using `MAX()`

```sql
SELECT MAX(sal) AS maximum_salary
FROM employee;
```

---

## 4. Display the minimum salary from employee table

📌 Using `MIN()`

```sql
SELECT MIN(sal) AS minimum_salary
FROM employee;
```

---

## 5. Display the average salary from employee table

📌 Using `AVG()`

```sql
SELECT AVG(sal) AS average_salary
FROM employee;
```

---

## 6. Display the maximum salary being paid to clerk

```sql
SELECT MAX(sal) AS max_clerk_salary
FROM employee
WHERE job = 'CLERK';
```

---

## 7. Display the maximum salary being paid in dept no 20

```sql
SELECT MAX(sal) AS max_salary_dept20
FROM employee
WHERE deptno = 20;
```

---

## 8. Display the minimum salary paid to any salesman

```sql
SELECT MIN(sal) AS min_salesman_salary
FROM employee
WHERE job = 'SALESMAN';
```

---

## 9. Display the average salary drawn by managers

```sql
SELECT AVG(sal) AS avg_manager_salary
FROM employee
WHERE job = 'MANAGER';
```

---

## 10. Display the total salary drawn by analyst working in dept no 40

```sql
SELECT SUM(sal) AS total_analyst_salary
FROM employee
WHERE job = 'ANALYST'
AND deptno = 40;
```

---

## 11. Display the names of the employee in Uppercase

📌 Using `UPPER()`

```sql
SELECT UPPER(ename) AS employee_name
FROM employee;
```

---

## 12. Display the names of the employee in Lowercase

📌 Using `LOWER()`

```sql
SELECT LOWER(ename) AS employee_name
FROM employee;
```

---

## 13. Display the names of the employee in Proper case

📌 Using `INITCAP()` (Oracle)

```sql
SELECT INITCAP(ename) AS employee_name
FROM employee;
```

---

## 14. Display the length of your name using appropriate function

📌 Example shown with name 'LAKSHYA'

```sql
SELECT LENGTH('LAKSHYA') AS name_length
FROM dual;
```

---

## 15. Display the length of all the employee names

📌 Using `LENGTH()`

```sql
SELECT ename, LENGTH(ename) AS name_length
FROM employee;
```

---
