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
### COALESCE
COALESCE( ) returns the first non-value in a list.
```
SELECT COALESCE(val1, val2, ..., val_n)
```
### CONNECTION_ID
CONNECTION_ID( ) returns the unique connection ID for the current connection.
```
SELECT CONNECTION_ID( )
```
### CONV
CONV( ) converts a number from one numeric base system to another and returns the result as a string value.
```
SELECT CONV(number, from_base, to_base)
```
### CONVERT
CONVERT( ) converts a value into the specified datatype or character set.
```
SELECT CONVERT(value, type)
```
### CURRENT_USER
CURRENT_USER( ) returns the user name and host name for the MySQL account that the server used to authenticate
the current client.
```
SELECT CURRENT_USER( )
```
### DATABASE
DATABASE( ) returns the name of the current database. Returns NULL if there is no current database.
```
SELECT DATABASE( )
```
### IF
IF( ) returns a value if a condition is TRUE or another value if a condition is FALSE.
```
SELECT IF(condition, value_if_true, value_if_false)
```
