# 🔹 RETRIEVING DATA – SET 2 (EMPLOYEE TABLE)

---

## 1. Employees who joined before 30-June-1980 or after 31-Dec-1981

📌 Using date condition with `<` and `>`

```sql
SELECT ename, hiredate 
FROM employee
WHERE hiredate < '30-JUN-80' 
   OR hiredate > '31-DEC-81';
```

---

## 2. Employees whose names have second alphabet 'A'

📌 Using LIKE with underscore `_`

```sql
SELECT ename 
FROM employee
WHERE ename LIKE '_A%';
```

---

## 3. Employees whose name is exactly five characters long

📌 Using five underscores (`_____`)

```sql
SELECT ename 
FROM employee
WHERE ename LIKE '_____';
```

---

## 4. Employees whose names have second alphabet 'A'

📌 Same as Question 2

```sql
SELECT ename 
FROM employee
WHERE ename LIKE '_A%';
```

---

## 5. Employees not working as Salesman, Clerk, or Analyst

📌 Using `NOT IN`

```sql
SELECT ename, job 
FROM employee
WHERE job NOT IN ('SALESMAN', 'CLERK', 'ANALYST');
```

---

## 6. Employee name with annual salary (sal * 12), highest first

📌 Using `ORDER BY` in descending order

```sql
SELECT ename, sal*12 AS annual_salary
FROM employee
ORDER BY annual_salary DESC;
```

---

## 7. Display name, sal, HRA, DA, PF, and Total Salary

📌  
- HRA = 15% of sal  
- DA = 10% of sal  
- PF = 5% of sal  
- Total Salary = (sal + hra + da) - pf  

```sql
SELECT 
    ename,
    sal,
    sal*0.15 AS hra,
    sal*0.10 AS da,
    sal*0.05 AS pf,
    (sal + (sal*0.15) + (sal*0.10) - (sal*0.05)) AS totalsal
FROM employee
ORDER BY totalsal DESC;
```

---

## 8. Update salary by 10% increment for employees not eligible for commission

📌 Commission is NULL

```sql
UPDATE employee
SET sal = sal + (sal*0.10)
WHERE comm IS NULL;
```

---

## 9. Employees whose salary becomes more than 3000 after 20% increment

📌 Checking condition without updating the table

```sql
SELECT ename, sal
FROM employee
WHERE sal + (sal*0.20) > 3000;
```

---

## 10. Employees whose salary contains at least 3 digits

📌 Salary between 100 and 999

```sql
SELECT ename, sal
FROM employee
WHERE sal BETWEEN 100 AND 999;
```

---
