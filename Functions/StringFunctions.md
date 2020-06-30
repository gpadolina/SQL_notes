## String Functions

### ASCII
ASCII() returns the ASCII value for the specified character.
```
SELECT ASCII(ProductName)
FROM Products;
```
### CHAR_LENGTH
CHAR_LENGTH() returns the length of a string (in characters). Same function as CHARACTER_LENGTH().
```
SELECT CHAR_LENGTH("FirstName LastName")
```
### CONCAT
CONCAT() adds two or more expressions together.
```
SELECT CONCAT(Address, " ", City, " ", State)
FROM Customers;
```
### CONCAT_WS()
CONCAT_WS() adds two or more expressions together with a separator.
```
SELECT CONCAT_WS(" ", Address, City, State)
FROM Customers;
```
