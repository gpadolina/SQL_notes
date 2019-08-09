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
