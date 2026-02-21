##1. Employees who joined before 30-June-1980 or after 31-Dec-1981

sql
SELECT ename, hiredate 
FROM employee
WHERE hiredate < '1980-06-30' 
   OR hiredate > '1981-12-31';
