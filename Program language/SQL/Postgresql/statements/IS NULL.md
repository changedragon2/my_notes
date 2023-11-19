### Syntax
```
value IS NULL
```
```
value IS NOT NULL
```

note this will return ***false***
```
NULL = NULL
```
### Example
```SQL
SELECT id, first_name, last_name, email, phone
FROM contact_demo
WHERE phone IS NULL;
```

Previous [Postgresql - LIKE](obsidian://open?vault=my_notes&file=Program%20language%2FSQL%2FPostgresql%2Fstatements%2FLIKE)

Next [Postgresql - Joins](obsidian://open?vault=my_notes&file=Program%20language%2FSQL%2FPostgresql%2Fstatements%2FJoins)