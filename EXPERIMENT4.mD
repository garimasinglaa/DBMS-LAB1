1️⃣ Employees who joined before 30-June-1980 or after 31-Dec-1981
SELECT ename, hiredate
FROM employee
WHERE hiredate < '1980-06-30'
   OR hiredate > '1981-12-31';
   2️⃣ Employees whose second letter is 'A'
SELECT ename
FROM employee
WHERE ename LIKE '_A%';
3️⃣ Employees whose name is exactly 5 characters long
SELECT ename
FROM employee
WHERE LENGTH(ename) = 5;
4️⃣ Employees whose second letter is 'A'
SELECT ename
FROM employee
WHERE ename LIKE '_A%';
5️⃣ Employees not working as Salesman, Clerk, or Analyst
SELECT ename
FROM employee
WHERE job NOT IN ('SALESMAN','CLERK','ANALYST');
6️⃣ Employee Name with Annual Salary (Highest First)
SELECT ename, sal*12 AS annual_salary
FROM employee
ORDER BY sal DESC;
7️⃣ Display ename, sal, hra, da, pf, totalsal

HRA = 15% of salary

DA = 10% of salary

PF = 5% of salary

Total Salary = (sal + hra + da) - pf

SELECT 
    ename,
    sal,
    sal*0.15 AS hra,
    sal*0.10 AS da,
    sal*0.05 AS pf,
    (sal + sal*0.15 + sal*0.10 - sal*0.05) AS totalsal
FROM employee
ORDER BY totalsal;
8️⃣ Update salary by 10% increment (Employees not eligible for commission)
UPDATE employee
SET sal = sal + sal*0.10
WHERE comm IS NULL;
9️⃣ Employees whose salary becomes more than 3000 after 20% increment
SELECT ename, sal
FROM employee
WHERE sal + sal*0.20 > 3000;
🔟 Employees whose salary contains at least 3 digits
SELECT ename, sal
FROM employee
WHERE LENGTH(sal) >= 3;
