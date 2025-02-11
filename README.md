# SQL_Project

# Project SQL Queries

This repository contains useful SQL queries for analyzing the `cleaned_file` dataset in the `project` database.

## Database Selection
```sql
USE project;
```

## Queries

### 1. Select all data from the table
```sql
SELECT * FROM cleaned_file;
```

### 2. Select specific columns (name and rating)
```sql
SELECT name, rating FROM cleaned_file;
```

### 3. Get all theaters with a rating of 5
```sql
SELECT * FROM cleaned_file 
WHERE rating = 5;
```

### 4. Get the average rating of all theaters
```sql
SELECT AVG(rating) AS avg_rating FROM cleaned_file;
```

### 5. Count the number of theaters per genre
```sql
SELECT genre, COUNT(*) FROM cleaned_file 
GROUP BY genre;
```

### 6. Get all theaters ordered by review count (descending)
```sql
SELECT * FROM cleaned_file 
ORDER BY review_count DESC;
```

### 7. Get theaters located in Saudi Arabia
```sql
SELECT * FROM cleaned_file 
WHERE location LIKE '%Saudi Arabia%';
```

### 8. Find theaters with a review count between 10,000 and 100,000
```sql
SELECT * FROM cleaned_file 
WHERE review_count BETWEEN 10000 AND 100000;
```

### 9. Get theaters that are movie theaters
```sql
SELECT * FROM cleaned_file 
WHERE genre LIKE '%Movie theater%';
```

### 10. Get all unique genres
```sql
SELECT DISTINCT genre FROM cleaned_file;
```


