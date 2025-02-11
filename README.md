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
<img src="https://github.com/user-attachments/assets/0d2d2a75-ae3d-48f8-a7ed-513fd1c1f362" alt="Value Counts Output" width="900"/>


### 2. Select specific columns (name and rating)
```sql
SELECT name, rating FROM cleaned_file;
```
<img src="https://github.com/user-attachments/assets/9ba053fa-100a-4777-82d5-c6169d592c34" alt="Value Counts Output" width="400"/>


### 3. Get all theaters with a rating of 5
```sql
SELECT * FROM cleaned_file 
WHERE rating = 5;
```
<img src="https://github.com/user-attachments/assets/07b7b1d5-78c4-4220-95d2-fffd2b0b182e" alt="Value Counts Output" width="900"/>


### 4. Get the average rating of all theaters
```sql
SELECT AVG(rating) AS avg_rating FROM cleaned_file;
```
<img src="https://github.com/user-attachments/assets/f8ad4835-d3e8-4f66-b949-36995aacbde2" alt="Value Counts Output" width="400"/>


### 5. Count the number of theaters per genre
```sql
SELECT genre, COUNT(*) FROM cleaned_file 
GROUP BY genre;
```
<img src="https://github.com/user-attachments/assets/b7ac8c26-676c-44f5-a8a7-1700bc55e94c" alt="Value Counts Output" width="400"/>


### 6. Get all theaters ordered by review count (descending)
```sql
SELECT * FROM cleaned_file 
ORDER BY review_count DESC;
```
<img src="https://github.com/user-attachments/assets/f40c9d09-fa7a-4d69-ae25-ecb6523687b0" alt="Value Counts Output" width="900"/>


### 7. Get theaters located in Saudi Arabia
```sql
SELECT * FROM cleaned_file 
WHERE location LIKE '%Saudi Arabia%';
```
<img src="https://github.com/user-attachments/assets/03e6a84f-5426-4a3a-93df-efe45855680b" alt="Value Counts Output" width="900"/>


### 8. Find theaters with a review count between 10,000 and 100,000
```sql
SELECT * FROM cleaned_file 
WHERE review_count BETWEEN 10000 AND 100000;
```
<img src="https://github.com/user-attachments/assets/157950c2-26fa-49aa-a3f3-6c2d851a2b2d" alt="Value Counts Output" width="900"/>


### 9. Get theaters that are movie theaters
```sql
SELECT * FROM cleaned_file 
WHERE genre LIKE '%Movie theater%';
```
<img src="https://github.com/user-attachments/assets/0f6da341-807f-46d6-8af3-f1da2c7895b9" alt="Value Counts Output" width="900"/>


### 10. Get all unique genres
```sql
SELECT DISTINCT genre FROM cleaned_file;
```

<img src="https://github.com/user-attachments/assets/d64010c5-1c3d-41f9-8667-7540bb65f601" alt="Value Counts Output" width="400"/>


