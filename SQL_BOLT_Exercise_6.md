# SQL_BOLT Review 1

## 1. List all the Canadian cities and their populations
```sql
SELECT CITY, POPULATION FROM NORTH_AMERICAN_CITIES
WHERE COUNTRY = 'Canada';
```

## 2. Order all the cities in the United States by their latitude from north to south
```sql
SELECT * FROM NORTH_AMERICAN_CITIES
WHERE COUNTRY = 'United States'
ORDER BY LATITUDE DESC;
```

## 3. List all the cities west of Chicago, ordered from west to east
```sql
SELECT * FROM NORTH_AMERICAN_CITIES
WHERE LONGITUDE < (
    SELECT LONGITUDE FROM NORTH_AMERICAN_CITIES
    WHERE CITY = 'Chicago'
)
ORDER BY LONGITUDE ASC;
```

## 4. List the two largest cities in Mexico (by population)
```sql
SELECT * FROM NORTH_AMERICAN_CITIES
WHERE COUNTRY = 'Mexico'
ORDER BY POPULATION DESC
LIMIT 2;
```

## 5. List the third and fourth largest cities (by population) in the United States and their population
```sql
SELECT CITY, POPULATION FROM NORTH_AMERICAN_CITIES
WHERE COUNTRY = 'United States'
ORDER BY POPULATION DESC
LIMIT 2 OFFSET 2;
```
