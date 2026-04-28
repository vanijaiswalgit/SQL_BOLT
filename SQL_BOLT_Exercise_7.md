# SQL_BOLT Exercise 7

## 1. Find the list of all buildings that have employees
```sql
SELECT DISTINCT BUILDING FROM EMPLOYEES;
```

## 2. Find the list of all buildings and their capacity
```sql
SELECT BUILDING_NAME, CAPACITY FROM BUILDINGS;
```

## 3. List all buildings and the distinct employee roles in each building (including empty buildings)
```sql
SELECT DISTINCT B.BUILDING_NAME, E.ROLE
FROM BUILDINGS B
LEFT JOIN EMPLOYEES E
ON B.BUILDING_NAME = E.BUILDING;
```
