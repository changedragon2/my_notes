#### Syntax
```SQL
SELECT
    select_list
FROM
    table_name
ORDER BY
    column_nameX [ ASC | DESC ];
```
```SQL
SELECT
    select_list
FROM
    table_name
ORDER BY
    column_nameX [ NULLS FIRST | NULLS LAST ];
```

#### Example
1. first name ascending, last name descending when with the same first name
```SQL
SELECT
    first_name, last_name
FROM
    actor
ORDER BY
    first_name ASC, last_name DESC;
```
2. LENGTH(str) returns the length of str
```SQL
SELECT
    first_name, LENGTH(first_name) len
FROM
    actor
ORDER BY
    len ASC;
```
3. null is last by default in ascending, whlile first by default in descending
```SQL
CREATE TABLE sort_demo(
    num INT
);
INSERT INTO sort_demo(num) VALUES(1),(2),(3),(null);
SELECT
    num
FROM
    sort_demo
ORDER BY
    num DESC NULLS LAST;
```