#### Syntax
```SQL
SELECT
    select_list
FROM
    table_name
WHERE
    condition
ORDER BY
    sort_expression;
```
1. order
FROM -> WHERE -> SELECT -> ORDER BY
2. condition in WHERE

| Operator | Description                                         |
| -------- | --------------------------------------------------- |
| =        | Equal                                               |
| >        | Grater than                                         |
| <        | Less thaan                                          |
| >=       | Grater than or equal                                |
| <=       | Less than or equal                                  |
| <> or != | Not equal                                           |
| AND      | Logical operator AND                                |
| OR       | Logical operator OR                                 |
| IN       | Return true if a value matches any value in a list  |
| BETWEEN  | Return true if a value is between a range of values |
| LIKE     | Return true if a value matches a pattern            |
| IS NULL  | Return true if value is null                        |
| NOT      | Negate the result of other operators                | 

#### Examples
1. AND
```SQL
SELECT first_name, last_name
FROM customer
WHERE first_name = 'Jamie' AND last_name = 'Rice';
```
2. OR
```SQL
SELECT first_name, last_name
FROM customer
WHERE first_name = 'Rodriguez' OR first_name = 'Anne';
```
3. IN
```SQL
SELECT first_name
FROM customer
WHERE first_name IN ('Anne', 'Ann', 'Annie');
```
4. LIKE
```SQL
SELECT first_name
FROM customer
WHERE first_name LIKE 'An%';
```
5. BETWEEN
```SQL
SELECT first_name, LENGTH(first_name) name_length
FROM customer
WHERE first_name = 'A%'  AND LENGTH(first_name) BETWEEN 3 AND 5
ORDER BY name_length ASC;
```
6. <> or !=
```SQL
SELECT first_name, last_name
FROM customer
WHERE first_name LIKE 'Bra%' AND last_name <> 'Motley';
```