### Syntax
```SQL
SELECT
    select_column
FROM
    table_name
ORDER BY
    sort_expression
LIMIT row_count OFFSET row_to_skip;
```


### Example
```SQL
SELECT
    film_id, title, release_year
FROM
    film
ORDER BY
    film_id
LIMIT 10;
```

2. id 6-15
```SQL
SELECT
    film_id, title, release_year
FROM
    film
ORDER BY
    film_id
LIMIT 10 OFFSET 5;
```