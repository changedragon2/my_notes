### Syntax
```SQL
value BETWEEN low AND high;

value NOT BETWEEN low AND high;
```


### Example
1. payment amount between 8 and 9
```SQL
SELECT customer_id, payment_id, amount
FROM payment
WHERE amount BETWEEN 8 AND 9;
```
2. payment amount not between 8 and 9
```SQL
SELECT customer_id, payment_id, amount
FROM payment
WHERE amount NOT BETWEEN 8 AND 9;
```
3. payment date
```SQL
SELECT customer_id, payment_id, amount, payment_date
FROM payment
WHERE payment_date BETWEEN '2007-02-07' AND '2007-02-15';
```