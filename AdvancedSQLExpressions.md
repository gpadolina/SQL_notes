## Conditional expressions
`IF... THEN...ELSE...ENDIF` is the most common conditional statement. SQL has a `CASE` statement and a `CASE` expression. The latter can be use in the following ways:
* Use the expression with search condition.
* Use the expression to compare a table field to a specified value.

### CASE with search conditions
This has the following syntax,
```
CASE
  WHEN condition_1 THEN result_1
  WHEN condition_2 THEN result_2
  ...
  WHEN condition_n THEN result_n
  ELSE result_m
END
```
Example updating values using CASE expression
```
UPDATE GRADES
SET MIDTERMS = CASE
    WHEN SCORE >= 90
      THEN 'A'
    WHEN SCORE >= 80 AND < 90
      THEN 'B'
    WHEN SCORE >= 70 AND < 80
      THEN 'C'
    ELSE 'D'
END;
```

### CASE with values
CASE with values has similar syntax with search conditions except condition is replaced with values
```
CASE test_value
  WHEN value_1 THEN result_1
  WHEN value_2 THEN result_2
  ...
  WHEN value_n THEN result_n
  ELSE result_m
```

### CASE NULLIF
```
UPDATE FLIGHT                                         # This is in a shorthand form
SET Connection = NULLIF(Connection, 'Chicago');
```

### CASE - COALESCE
This has the following form
```
CASE
  WHEN value_1 IS NOT NULL
    THEN value_1
  WHEN value_2 IS NOT NULL
    THEN value_2
  ...
  WHEN value_n IS NOT NULL
    THEN value_n
  ELSE NULL
END
```

## Data-type conversions

### CAST
```
SELECT *
FROM CUSTOMERS
WHERE CUSTOMERS.ID = CAST (PROSPECT.ID AS INTEGER)
```
