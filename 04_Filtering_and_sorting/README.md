
# [Filtering and sorting Query results](https://sqlbolt.com/lesson/filtering_sorting_query_results)

> **DISTINCT** : SQL provides a convenient way to discard rows that have a duplicate column value by using the __DISTINCT__ keyword.
--- 
## Example-1 
```sql
-- Select query with unique results
SELECT DISTINCT column, another_column, …
FROM mytable
WHERE condition(s);
```
> __DISTINCT__ keyword will blindly remove duplicate rows 

> Alternative __GROUP BY__ (For Better Output)

--- 

<mark> NOTE :</mark> SQL provides a way to sort your results by a given column in ascending or descending order using the __ORDER BY__ clause.

## Ordering results
```sql
-- Select query with ordered results
-- List all directors of Pixar movies (alphabetically), without duplicates 

SELECT DISTINCT director FROM movies
ORDER BY director ASC;

```
> This code list all the directors Alphabetically without duplicates. 

--- 
## Limiting results to a subset
### Example - 2
```sql
SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC
LIMIT num_limit OFFSET num_offset;

```
### Real solved Problem 
```sql
-- Select query with ordered results
-- List the first five Pixar movies sorted alphabetically 

SELECT title FROM movies
ORDER BY title ASC
LIMIT 5;

```
![The solve looks liek](1.png)
> This code lists First 5 Pixer Movies Alphabetically. 

