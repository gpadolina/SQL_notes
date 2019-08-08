Rapid application development (RAD) such Microsoft Access development environment and SQL DDL can be used to build databases but being proficient at both can be worthwhile. 

### Indexing

* *Index* - An index is a table of pointers. Each row in the index points to a corresponding row in the data table.
* Indexes can be updated much faster than sorting a table and are necessary for large tables.
* Since primary keys are the fastest eay to access data, they should always be indexed.
* Indexing frequently used fields to access records is always a good idea.
* SQL doesn't provide a way to create index. DBMS provide their own implementations but most common is using `CREATE INDEX`.

SQL data definition language can be used in Microsoft Access to build databases just as how you would build databases in other server DBMS.
```
SELECT *
FROM CUSTOMERS
WHERE State = 'CA';
```

### Creating a table
```
CREATE TABLE CUSTOMERS (
    CustomerID          INTEGER         PRIMARY KEY,
    FirstName           CHAR (15),
    LastName            CHAR (15),
    Adress              CHAR (15),
    City                CHAR (15),
    State               CHAR (15),
    PhoneNumber         CHAR (15);
```

### Altering a table
```
ALTER TABLE CLIENTS
ADD COLUMN Email CHAR(20);

ALTER TABLE CLIENTS
DROP COLUMN PhoneNumber;
```

### Deleting a table
```
DROP TABLE CLIENTS;
```

### Deleting an index
Indexes will be deleted when you drop a table using the `DROP TABLE` statement.
