### Usage
relationship
![inner_join](inner_join.png)
a customer -> multiple payments, one payment -> one customer
a staff -> multiple payments, one payment -> a staff
### Example
```SQL
SELECT
    c.customer_id,
    c.first_name || ' ' || c.last_name "Customer Full Name",
    c.email,
    amount,
    payment_date,
    s.first_name || ' ' || s.last_name "Staff Full Name"
FROM
    customer c
INNER JOIN payment p ON p.customer_id = c.customer_id
INNER JOIN staff s ON s.staff_id = p.staff_id
ORDER BY c.customer_id;
```


Previous [Postgresql - Table Alias](obsidian://open?vault=my_notes&file=Program%20language%2FSQL%2FPostgresql%2Fstatements%2FTable%20Alias)