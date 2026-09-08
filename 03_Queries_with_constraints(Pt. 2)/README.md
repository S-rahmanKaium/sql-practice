# [Queries with constraints (Pt. 2)](https://sqlbolt.com/lesson/select_queries_with_constraints_pt_2)

> **WHERE** : The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.
--- 
## Example 
```sql
-- Select query with constraints
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;

```
> SQL supports a number of useful operators to do things like case-insensitive string comparison and wildcard pattern matching

| Operator | Condition | Example |
|:---:|---|---|
| `=` | Exact match | `col_name = "abc"` |
| `!=` / `<>` | Not equal | `col_name != "abcd"` |
| `LIKE` | Pattern match | `col_name LIKE "ABC"` |
| `NOT LIKE` | Does not match pattern | `col_name NOT LIKE "ABCD"` |
| `%` | Matches 0 or more characters | `col_name LIKE "%AT%"` |
| `_` | Matches exactly 1 character | `col_name LIKE "AN_"` |
| `IN (...)` | Matches any value in a list | `col_name IN ("A", "B", "C")` |
| `NOT IN (...)` | Doesn't match any value in a list | `col_name NOT IN ("D", "E", "F")` |

<mark> NOTE :</mark> `All strings must be quoted so that the query parser can distinguish words in the string from SQL keywords.`

## Second Code block 

```sql
-- Select query with constraints
-- Find all the WALL-* movies
SELECT title --> These are columns
FROM movies --> Table name
WHERE 
    title like "%WALL-%" 
 ; --> Condition checking

```
> This Code Block will list title all the movies That Name **WALL-***.  

