# SQL_BOLT Exercise 9

## 1. List all movies and their combined sales in millions of dollars
```sql
SELECT M.TITLE, (B.DOMESTIC_SALES + B.INTERNATIONAL_SALES)/1000000 AS TOTAL_SALES_MILLIONS
FROM MOVIES M
JOIN BOXOFFICE B
ON M.ID = B.MOVIE_ID;
```

## 2. List all movies and their ratings in percent
```sql
SELECT M.TITLE, B.RATING * 10 AS RATING_PERCENT
FROM MOVIES M
JOIN BOXOFFICE B
ON M.ID = B.MOVIE_ID;
```

## 3. List all movies that were released on even number years
```sql
SELECT *
FROM MOVIES
WHERE YEAR % 2 = 0;
```
