### Syntax
```SQL
table_name AS alias_name
```
or omit AS
```SQL
table_name alias_name
```

### Usage
1. using table alias for the long table name
```SQL
a_very_long_table_name.column_name
```
alias
```SQL
a_very_long_table_name AS alias
```
```SQL
alias.column_name
```
2. using table alias in join clauses
for multiple tables that have the same column name
```SQL
table_name.column_name
```
to make the query short, use the table aliases for the table names listed on FROM and INNER JOIN clauses
```SQL
SELECT c.customer_id, first_name, amount, payment_date
FROM customer c
INNER JOIN payment p ON p.customer_id = c.customer_id
ORDER BY payment_date DESC;
```
3. using table alias in self-join
referencing the same table multiple times within a query results an error

Previous [Postgresql - joins](obsidian://open?vault=my_notes&file=Program%20language%2FSQL%2FPostgresql%2Fstatements%2FJoins)

Next [Postgresql - INNER JOIN](obsidian://open?vault=my_notes&file=Program%20language%2FSQL%2FPostgresql%2Fstatements%2FINNER%20JOIN)