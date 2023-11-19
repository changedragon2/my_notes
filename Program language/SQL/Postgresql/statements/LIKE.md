### Syntax
```SQL
value LIKE pattern
```
```SQL
value NOT LIKE pattern
```
case-insensitively
```SQL
value ILIKE pattern
```
operator
```
Operator    Equivalent
  ~~           LIKE
  ~~*          ILIKE
  !~~         NOT LIKE
  !~~*        NOT ILIKE
```
pattern
```
%    matches any sequences of zero or more characters
_    matches any single character
```

### Example
```SQL
SELECT first_name, last_name
FROM customer
WHERE first_name LIKE '%er%'
ORDER BY first_name;
```


Previous [Postgresql - IN](obsidian://open?vault=my_notes&file=Program%20language%2FSQL%2FPostgresql%2Fstatements%2FIN)

Next [Postgresql - IS NULL](obsidian://open?vault=my_notes&file=Program%20language%2FSQL%2FPostgresql%2Fstatements%2FIS%20NULL)