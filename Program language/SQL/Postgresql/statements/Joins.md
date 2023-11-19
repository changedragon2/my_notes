### Syntax
1. inner join
```SQL
SELECT selct_columns
FROM table_one
INNER JOIN table_two ON table_one.column_a = table_two.column_b;
```
2. left join / left outer join
```SQL
SELECT select_columns
FROM table_one
LEFT JOIN table_two ON table_one.column_a = table_two.column_b;
```
3. right join / right outer join
```SQL
SELECT select_columns
FROM table_one
RIGHT JOIN table_two ON table_one.column_a = table_two.column_b;
```
4. full join / full outer join
```SQL
SELECT select_columns
FROM table_one
FULL JOIN table_two ON table_one.column_a = table_two.column_b;
```

### View
![joins](joins.png)

Previous [Postgresql - IS NULL](obsidian://open?vault=my_notes&file=Program%20language%2FSQL%2FPostgresql%2Fstatements%2FIS%20NULL)

Next [Postgresql - Table Aliases](obsidian://open?vault=my_notes&file=Program%20language%2FSQL%2FPostgresql%2Fstatements%2FTable%20Alias)