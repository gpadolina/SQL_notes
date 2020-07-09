## Advanced Functions

### BIN
BIN( ) returns a binary representation of a number as a string value.
```
SELECT BIN(number)
```
### BINARY
BINARY( ) converts a value to a binary stirng. This is equivalent to CAST(value AS BINARY).
```
SELECT BINARY value
```
### CASE
CASE statements goes through conditions and return a value when the first condition is met. If no conditions
are true, it will return the value in the ELSE clause. If there is no ELSE parts and no conditions are true,
it returns NULL.
```
CASE
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    WHEN conditionN THEN resultN
    ELSE result
END;
```
### CAST
CAST( ) converts a value into the specified datatype.
```
SELECT CAST(value AS datatype)
```
