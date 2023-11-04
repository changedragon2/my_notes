#### Syntax
```SQL
SELECT column_name AS alias_name FROM table_name;
```
```SQL
SELECT column_name alias_name FROM table_name;
```
```SQL
SELECT expression AS alias_name FROM table_name;
```

Alias exaple
1. alias column
```SQL
SELECT
    column_name AS alias_name
FROM
    table_name;
```
2. alias expression
```SQL
SELECT
    column_name1 || ' ' || column_name2 AS alias_name
FROM
    table_name;
```
3. alias name contains space with double quotes " "
```SQL
SELECT
    first_name || ' ' || last_name AS "Full Name"
FROM
    table_name;
```
4. alias keyword 'AS' is optional, you can omit it
```SQL
SELECT
    column_name alias_name
FROM
    table_name;
```