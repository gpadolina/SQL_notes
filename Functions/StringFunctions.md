## String Functions

### ASCII
ASCII( ) returns the ASCII value for the specified character.
```
SELECT ASCII(ProductName)
FROM Products;
```
### CHAR_LENGTH
CHAR_LENGTH( ) returns the length of a string (in characters). Same function as CHARACTER_LENGTH().
```
SELECT CHAR_LENGTH("FirstName LastName")
```
### CONCAT
CONCAT( ) adds two or more expressions together.
```
SELECT CONCAT(Address, " ", City, " ", State)
FROM Customers;
```
### CONCAT_WS
CONCAT_WS( ) adds two or more expressions together with a separator.
```
SELECT CONCAT_WS(" ", Address, City, State)
FROM Customers;
```
### FIELD
FIELD( ) returns the index position of a value in a list of values. This is case-insensitive.
```
FIELD(value, val1, val2, val3, ...)         # value: The value to search for in the list.
                                            # val1:val3: The list of values to search.
```
### FIND_IN_SET
FIND_IN_SET( ) returns the position of a string within a list of strings.
```
FIND_IN_SET(string, string_list)            # string: The string to search for.
                                            # string_list: The list of string values to be searched.
```
