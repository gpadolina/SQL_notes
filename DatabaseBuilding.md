Rapid application development (RAD) such Microsoft Access development environment and SQL DDL can be used to build databases but being proficient at both can be worthwhile. 

### Indexing

* *Index* - An index is a table of pointers. Each row in the index points to a corresponding row in the data table.
* Indexes can be updated much faster than sorting a table.
* Since primary keys are the fastest eay to access data, they should always be indexed.
* Indexing frequently used fields to access records is always a good idea.

SQL data definition language can be used in Microsoft Access to build databases just as how you would build databases in other server DBMS.
```
SELECT *
FROM CUSTOMERS
WHERE State = 'CA';
```

### Creating a table
