SQL Standard Statement

### Syntax
```SQL
SELECT select_columns
FROM table_name
OFFSET row_to_skip { ROW | ROWS }
FETCH { FIRST | LAST } row_counts { ROW | ROWS } ONLY;
```
row_to_skip >= 0, 0 by default
row_counts >=1, 1 by default
use FETCH with ORDER BY to return ordered rows

### Example
1. return first 5 order by film_id
```SQL
SELECT film_id, title
FROM film
ORDER BY film_id
FETCH FIRST 5 ROWS ONLY;
```
2. return first 6-10
```SQL
SELECT film_id, title
FROM film
ORDER BY film_id
OFFSET 5 ROWS
FETCH FIRST 5 ROWS ONLY;
```