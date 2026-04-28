# SQL_BOLT Exercise 8

## 1. Find the name and role of all employees who have not been assigned to a building
```sql
SELECT NAME, ROLE FROM EMPLOYEES
WHERE BUILDING IS NULL;
```

## 2. Find the names of the buildings that hold no employees
```sql
SELECT B.BUILDING_NAME
FROM BUILDINGS B
LEFT JOIN EMPLOYEES E
ON B.BUILDING_NAME = E.BUILDING
WHERE E.BUILDING IS NULL;
```
