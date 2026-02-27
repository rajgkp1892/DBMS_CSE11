# Assignment 6

**Date:** 13-02-2026

## Date Functions and CASE Function on `emp` and `dept` Tables

---

## Aim

To perform queries using the `CASE` function, date functions, and string formatting on the `emp` and `dept` tables.

---

## Table Reference

```sql
SELECT * FROM dept;
```

---

## 1. Display empno, ename and Department Name Instead of Department Number

```sql
SELECT empno, ename,
CASE deptno
    WHEN 10 THEN 'RESEARCH'
    WHEN 20 THEN 'ACCOUNTING'
    WHEN 30 THEN 'SALES'
    WHEN 40 THEN 'OPERATIONS'
END AS DEPT_NAMES
FROM emp;
```

---

## 2. Display Age in Days

```sql
SELECT DATEDIFF(CURDATE(), '2006-10-04') AS AGE_IN_DAYS;
```

---

## 3. Display Age in Months

```sql
SELECT TIMESTAMPDIFF(MONTH, '2006-10-04', CURDATE()) AS AGE_IN_MONTHS;
```

---

## 4. Display Current Date in Formatted Style

```sql
SELECT DATE_FORMAT(CURDATE(), '%D %M %W %Y') AS CURRENT_DATE;
```

---

## 5. Display: "Employee has joined the company on <date>"

```sql
SELECT CONCAT(
    ename,
    ' has joined the company on ',
    DATE_FORMAT(hiredate, '%D %M %W %Y')
) AS REQUIRED_FORMAT
FROM emp;
```

---

## 6. (Part of Question 5 – formatted join message already displayed)

---

## 7. Find the Nearest Saturday After C
