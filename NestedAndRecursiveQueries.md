To protect the data's integrity by avoiding modification anomalies, we must normalize the database. Normalization involves breaking up a single table into multiple tables. We can then use relational operators to pull data from multiple tables. But another way to pull data from two or more tables is nested query.

Subqueries are located within the `WHERE` clause. This provides the search conditions for the `WHERE` clause.

### Subqueries using the keyword IN
This has the following syntax:
```
SELECT column_list
FROM table
WHERE expression
IN (subquery);
```
Example:
```
SELECT Items
FROM INVENTORY
WHERE ItemID IN           # IN can be replaced with NOT IN
( SELECT ItemID
  FROM ORDERS
  WHERE Class = 'B');
```

### EXISTS
```
SELECT *
FROM table
WHERE EXISTS
( SELECT *
  FROM table_2
  WHERE condition );
```

### UPDATE
```
UPDATE table_name
SET column = value
WHERE (condition);          # 'condition' can be a nested query
```

### DELETE
```
DELETE FROM table
WHERE (condition);          # 'condition can be a nested query
```

## Recursive query

```
WITH RECURSIVE
expression_name (column_list)
AS (
  initial_query
  UNION
  recursive_query
   )
SELECT *
FROM expression_name
```
