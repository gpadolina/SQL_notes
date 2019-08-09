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
