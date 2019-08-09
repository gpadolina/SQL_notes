## Manipulation

### Retrieving data
Retrieving data has the following form
```
SELECT column_list
FROM table_name
WHERE condition;

SELECT FirstName, LastName      # * can be used to select all columns
FROM CUSTOMER
WHERE State = 'CA' AND Age <= 40;
```

### Creating a view
```
CREATE VIEW CUSTOMER_INFO
AS SELECT CUSTOMERS.CustomerID, OrderDate, ShippingDate
FROM CUSTOMERS, ORDERS
WHERE CUSTOMERS.CustomerID = ORDERS.CustomerID
AND ORDERS.State = 'CA';
```
Updating a view can be done by doing the following
```
UPDATE view_name SET column_name = condition;
```

### Adding new data
```
INSERT INTO table_name [(column_1, column_2, ..., column_n)]
VALUES (value_1, value_2, ..., value_n);
```

### Transferring columns and rows between table
```
SELECT FirstName, LastName
FROM PROSPECT
WHERE State = 'CA'
UNION 
SELECT FirstName, LastName
FROM CUSTOMERS
Where State = 'CA';

OR

INSERT INTO PROSPECT
SELECT FirstName, LastName
FROM CUSTOMERS
WHERE State = 'CA';
```

### Updating existing data
```
UPDATE table_name
SET column_1 = expression_1, column_2 = expression_2, ..., column_n = expression_n
WHERE condition;

UPDATE CUSTOMERS
SET AreaCode = '415'
WHERE City = 'San Francisco';
```

### Transferring data using merge
```
MERGE INTO table_name
USING table_name2
ON (table_name.column = table_name2.column)
WHEN MATCHED THEN DELETE                        # Optional
WHEN NOT MATCHED THEN INSERT                    # Optional
(table_name.column, table_name.column_n)
VALUES (table_name2.column, value);
```

### Deleting data
```
DELETE FROM table
WHERE column = condition, ..., column_n = condition_n
```

## Temporal data
* *Period* - A named table component that captures the period start and period end.
* *Valid time* - Time during which a row in a table correctly reflects reality.
* *Transaction time* - Time during which a row is committed to or recorded in a database.

```
CREATE TABLE STUDENT_INFO (
  StudentID         INTEGER,
  StudentStart      DATE,
  StudentEnd        DATE,
  StudentYear       CHAR(15),
  PERIOD FOR StuPeriod (StudentStart, StudentEnd));
```
Examples:
```
SELECT *
FROM STUDENT_INFO
WHERE StudentStart <= CURRENT_DATE()
AND StudentEnd > CURRENT_DATE();
```

```
SELECT *
FROM STUDENT_INFO
WHERE StuPeriod CONTAINS CURRENT_DATE();
```

```
SELECT *
FROM STUDENT_INFO
WHERE StuPeriod OVERLAPS
PERIOD (DATE('2019-01-01'), DATE('2019-01-01'));
```

## Value specification

### Variables
It's best to replace literals with variables when doing updates.
```
UPDATE INVENTORY
  SET Price = Cost * :multiplierA
  WHERE Product = 'Selvedge'
  AND Class = 'A'
UPDATE INVENTORY
  SET Price = Cost * :multiplierB
  WHERE Product = 'Coat'
  AND Class = 'B'
UPDATE INVENTORY
  SET Price = Cost * :multiplierC
  WHERE Product = 'Dress'
  AND Class = 'C';
```
When we need to update the inventory again, we can just the value of the variables to make it easier.
These are called host variables when used in embedded SQL.

## Functions

### Substring
We can extract a subtring from a string by doing the following
```
SUBSTRING (string_value FROM start [FOR length])

SELECT *
FROM INVENTORY
WHERE SUBTRING (Shirts FROM 5 FOR 4) = 'Solid';
```

### Upper
Converts a character string to all-uppercase.
```
UPPER ('Technology')
```

### Lower
The opposite of upper.
```
LOWER ('TECHNOLOGY')
```

### Trim
```
TRIM (LEADING ' ' FROM ' cat ')
TRIM (TRAILING ' ' FROM ' cat ')
TRIM (BOTH ' ' FROM ' cat ')
```

### Position
Searches for a specified target string within the source.
```
POSITION (target IN source [USING char length units])    # character string syntax
POSITION (target IN source)                              # binary string syntax
```

Other functions are available. Please see a documentation.
