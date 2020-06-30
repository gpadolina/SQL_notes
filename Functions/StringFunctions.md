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
### FORMAT
FORMAT( ) formats a number to a format like "###,###.##" then returns the result as a string.
```
FORMAT(number, decimal_places)              # number: The number to be formatted.
                                            # decimal_places: The number of decimal places for the number.
```
### INSERT
INSERT( ) inserts a string within a string at the specified position and for a certain number of characters.
```
INSERT(string, position, number, string2)   # string: The string that will be modified.
                                            # position: The position where to insert string2.
                                            # number: The number of characters to replace.
                                            # string2: The string to be inserted.
```
### INSTR
INSTR( ) returns the position of the first occurence of a string in another string.
```
INSTR(string, string2)                      # string: The string that will be searched.
                                            # string2: The string to search for in string.
```
### LCASE
LCASE( ) converts a string to a lower-case.
```
LCASE(text)
```
### LEFT
LEFT( ) extracts a number of characters from a string starting from the left.
```
LEFT(string, number_of_chars)               # string: The string to extract from.
                                            # number_of_chars: The number of characters to extract.
```
