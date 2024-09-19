# SQL Queries for Learning

On the journey of getting acquainted with SQL, I have tried a few queries, and I thought it’s better to share them here. This collection of queries will help beginners and learners practice SQL concepts across different topics such as basic queries, string manipulation, and ordering.

## 1. Basic Select Queries

These queries demonstrate how to select data from tables based on conditions.

```sql
SELECT * FROM employees WHERE department = 'HR';
SELECT "department" FROM Worker;
SELECT DISTINCT(department) FROM Worker;
```

## 2. String Manipulation Queries

These queries help you manipulate string values, such as changing case, removing white spaces, and replacing characters.
#### Convert to Uppercase :
This query converts the first_name column values 
```sql
to uppercase.
SELECT UPPER(first_name) AS WORKER_NAME FROM Worker WHERE first_name = 'Amithab';
```
#### Find Position of a Character in String
This query finds the position of a specific character (e.g., 'a') within the first_name.
```sql
SELECT POSITION('a' IN 'first_name') AS WORKER_NAME FROM Worker WHERE first_name = 'Amithab';
```
#### Trim White Spaces
This query removes extra white spaces from the first_name column.
```sql
SELECT TRIM(first_name) AS "FIRST_NAME" FROM Worker;
```
#### Replace Characters in String
This query replaces all occurrences of lowercase 'a' with uppercase 'A' in the first_name column.
```sql
SELECT REPLACE(first_name, 'a', 'A') AS "FIRST_NAME" FROM Worker;
```
## 3. Concatenation Queries
These queries concatenate first_name and last_name to create a full name for each worker.
```sql
SELECT first_name || ' ' || last_name AS "NAME" FROM Worker;
```
## 4. Sorting and Filtering Queries
Learn how to order results and filter data with conditions.
#### Order by Multiple Columns
This query orders the workers by first_name in descending order, and in case of ties, by department in ascending order.
```sql
SELECT * FROM Worker ORDER BY first_name DESC, department ASC;
```
#### Filter with Pattern Matching
This query finds workers whose first_name contains the letter 'a' (case-insensitive search).
```sql
SELECT * FROM Worker WHERE first_name ILIKE '%a%';
```
## 5. Fetching Records
These queries help you limit and fetch specific records, such as getting the last record from a table.

This query fetches the last record from the Worker table by using an OFFSET equal to the total number of rows minus one.
```sql
SELECT * FROM Worker OFFSET (SELECT COUNT(*) FROM Worker) - 1;
```


## Repository Goals
This repository is intended to serve as a practice ground for SQL learners, with examples covering common tasks. Feel free to contribute more queries or improve existing ones!


### Key Markdown Features:
- **Headings**: Used `#`, `##`, and `###` for different levels of headers.
- **Code Blocks**: Each SQL query is enclosed within three backticks (` ```sql `), ensuring that it is displayed as a properly formatted code block.
- **Subsections**: Organized into subsections for better readability. Each query has a small description to explain its purpose.

This will make the `README.md` well-organized and friendly for learning SQL on GitHub!
