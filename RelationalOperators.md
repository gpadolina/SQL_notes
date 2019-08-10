These includes `UNION`, `INTERSECTION`, `EXCEPT`, and `JOIN`.

### UNION
Enables us to draw information from two or more tables with the same structure such as having the same number of columns and identical data types. This kind of union eliminates duplicate rows and retrieves data in any of the source tables.
```
SELECT *
FROM CUSTOMERS
UNION
SELECT *
FROM PROSPECT
```
They must meet the criteria for the `UNION` to work.

### UNION ALL
This is similar to `UNION` except it preserves duplicate rows.
```
SELECT *
FROM CUSTOMERS
UNION ALL
SELECT *
FROM PROSPECT
```

### INTERSECT
`INTERSECT` only retrieves rows that appear in all source tables.
```
SELECT *
FROM CUSTOMERS
INTERSECT
SELECT *
FROM PROSPECT
```

`INTERSECT ALL` adds duplicates to the result.

### EXCEPT
`EXCEPT` returns all rows in the first table that does not appear in the second.
```
SELECT *
FROM CUSTOMERS
EXCEPT
SELECT *
FROM PROSPECT;
```

## JOINS

### CROSS JOINS
`CROSS JOINS` produce a cartesian product of two tables.
```
SELECT *
FROM CUSTOMERS, PROSPECT

# is similar to

SELECT *
FROM CUSTOMERS CROSS JOIN PROSPECT;
```

### CONDITION JOIN
```
SELECT *
FROM table_1 JOIN table_2
ON table_1.column = table_2.column;
```

### INNER JOIN
`INNER JOIN` removes all rows from the result table that don't have corresponding rows in both source tables.
```
SELECT *
FROM table_1
INNER JOIN table_2
ON table_1.column_name = table_2.column_name;
```

### LEFT OUTER JOIN
Preserves unmatched rows.
```
SELECT CUSTOMERS.CustomerName, PROSPECT.CustomerName
FROM CUSTOMERS
LEFT JOIN PROSPECT
ON CUSTOMERS.column = PROSPECT.column
```

### RIGHT OUTER JOIN

```
SELECT *
FROM CUSTOMERS C
RIGHT JOIN PROSPECT P
ON P.ID = C.ID
RIGHT JOIN ORDERS O
ON O.ID = P.ID
```
