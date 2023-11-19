### Syntax
```SQL
value IN (value1, value2, ...)
```
subquery
```SQL
value IN (SELECT select_column FROM table_name)
```

### Example
1. select return_date in 2005-05-27
```SQL
SELECT customer_id, rental_id, return_date
FROM rental
WHERE CAST (return_date AS DATE) = '2005-05-27'
ORDER BY customer_id;
```

2. select in subquery
```SQL
SELECT customer_id, first_name, last_name
FROM customer
WHERE customer_id IN (
    SELECT customer_id
    FROM rental
    WHERE CAST (return_date AS DATE) = '2005-05-27'
)
ORDER BY customer_id;
```


Previous []()

Next [Postgresql - LIKE](obsidian://open?vault=my_notes&file=Program%20language%2FSQL%2FPostgresql%2Fstatements%2FLIKE)