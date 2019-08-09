### Retrieving
Retrieving data has the following form
```
SELECT column_list
FROM table_name
WHERE condition;

SELECT FirstName, LastName      # * can be used to select all columns
FROM CUSTOMER
WHERE State = 'CA' AND Age <= 40;
```
