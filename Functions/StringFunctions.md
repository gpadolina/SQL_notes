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
### LENGTH
LENGTH( ) returns the length of a string.
```
LENGTH(string)
```
### LOCATE
LOCATE( ) returns the position of the first occurence of a substring in a string. This is case-insensitive.
```
LOCATE(substring, string, start)            # start: The starting position for the search. This is optional.
```
### LOWER
LOWER( ) converts a string to lower-case.
```
LOWER(text)
```
### LPAD
LPAD( ) left-pads a string with another string.
```
LPAD(string, length, lpad_string)           # string: The original string.
                                            # length: The length of the string after it has been left-padded.
                                            # lpad_string: The string to left-pad to original string.
```
### LTRIM
LTRIM( ) removes leading spaces from a string.
```
LTRIM(string)
```
### MID
MID( ) extracts a subtring from a string starting at any position.
```
MID(string, start, length)                  # start: The start position. Can be positive or negative number.
                                            # length: The number of characters to extract.
```
### POSITION
POSITION( ) returns the position of the first occurence of a subtring in a string. This is case-insensitive.
```
POSITION(substring IN string)
```
### REPEAT
REPEAT( ) repeats a string as many times as specified.
```
REPEAT(string, number)
```
### REPLACE
REPLACE( ) replaces all occurrences of a substring within a string with a new substring.
```
REPLACE(string, from_string, new_string)    # string: The original string.
                                            # from_string: The substring to be replaced.
                                            # new_string: The new replacement substring.
```
### REVERSE
REVERSE( ) reverses a string and returns the result.
```
REVERSE(string)
```
### RIGHT
RIGHT( ) extracts a number of characters from a string starting from right.
```
RIGHT(string, number_of_chars)
```
### RPAD
RPAD( ) right-pads a string with another string to a certain length.
```
RPAD(string, length, rpad_string)           # string: The original stirng.
                                            # length: The length of the string after it has been right-padded.
                                            # rpad_string: The string to right-pad to original string.
```
### RTRIM
RTRIM( ) removes trailing spaces from a string
```
RTRIM(string)
```
### SPACE
SPACE( ) returns a string of the specified number of space characters.
```
SPACE(number)                               # number: The number of space characters to return.
```
### STRCMP
STRCMP( ) compares two strings.
```
STRCMP(string1, string2)                    # returns 0 if string1 = string2
                                            # returns -1 if string1 < string2
                                            # returns 1 if string1 > string2
```
### SUBSTR
SUBSTR( ) extracts a substring from a string starting at any position. This function is the same as MID( ) and SUBSTRING( ).
```
SUBSTR(string, start, length)               # string: The string to extract from.
                                            # start: The start position. Can be negative or positive number.
                                            # length: The number of characters to extract. If omitted, the the whole string
                                            # will be returned from the start position.
```
