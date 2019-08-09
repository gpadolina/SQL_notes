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
