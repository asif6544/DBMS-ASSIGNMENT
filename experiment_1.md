# 🧪 Experiment 1 – SQL Commands on EMPLOYEE_MASTER

## 🎯 Objective
To perform CREATE, DELETE, UPDATE, ALTER, and DROP operations on a table using SQL.

---



```sql
-- 1. Create EMPLOYEE_MASTER table with data from EMPLOYEE
CREATE TABLE EMPLOYEE_MASTER AS 
SELECT * FROM EMPLOYEE;

-- 2. Delete all records where DEPTNO = 10
DELETE FROM EMPLOYEE_MASTER
WHERE DEPTNO = 10;

-- 3. Increase 10% salary for employees in DEPTNO = 20
UPDATE EMPLOYEE_MASTER
SET SAL = (SAL + IFNULL(COMM,0)) * 1.10
WHERE DEPTNO = 20;

-- 4. Modify SAL column datatype to DECIMAL(10,2)
ALTER TABLE EMPLOYEE_MASTER
MODIFY SAL DECIMAL(10,2);

-- 5. Drop EMPLOYEE_MASTER table
DROP TABLE EMPLOYEE_MASTER;
