* *Database* - A collection of integrated records. Consist of data and metadata.
  * Personal database
  * Departamental database
  * Enterprise database
* *Metadata* - Describes the data's structure within the database.
* *Record* - A representation of some physical or conceptual object. Each record has multiple attributes.
* *Database management system(DBMS)* - A set of programs used to define, administer, and process databases and their data.
* *NoSQL databases* - Lack the structure of relational databases and do not use SQL.
* *Relational databases* - Can be modified without affecting the data in the other tables if the table is not a parent table.
* *Relation* - Two-dimensional array of rows and columns that contains single valued entries and no duplicate rows. No two rows may be identical and each cell in the array can have only one value.
* *Views (or virtual tables)* - Views allow you to look at data but they are not part of the data and have no independent existence.
* *SQL* - The most widely used tool for communicating with a relational database and is not a procedural language.
* *Query* - A question you ask the database that retrieves the data.
* *SQL statements* - Perform functions for data handling such as defining, manipulating, and controling data.
* *Reserved words* - Some words with special significance within SQL.
* *Null values* - A field that does not contain a data item has a null value.
  * A null value is not the same as a value with zero in a numeric field.
  * A null value is not the same as blank in a character field.
* *Constraints* - Restrictions to the data that someone can enter into a database table.
* *Data Definition Language (DDL)* - Use to create a database, modify its structure, and erase it.
* *Data Manipulation Language (DML)* - Performs database maintenance like entering, changing, removing, and retrieving data.
* *Data Control Language (DCL)* - Protect the database from being corrupted and provide security.
* *Physical schema* - Represent the physical arrangement of the data and its associated items such as indexes.
* *Catalog* - Collection of schemas.

### Creating a database
1. Identify all tables.
2. Define the columns that each table must contain.
3. Give each table a primary key that is unique.
4. Make sure that every table in the database has at least one column in common with one another.
5. Ensure the prevention of insertion, deletion, and update anomalies.

### Creating a table
```
CREATE TABLE CLIENTS (
  FirstName     CHAR (10),     NOT NULL
  LastName      CHAR (10),     NOT NULL,
  Age           CHAR (10),
  Street        CHAR (10),
  City          CHAR (10),
  State         CHAR (10) );
```

### Altering a table
```
ALTER TABLE
```

### Dropping a table
```
DROP TABLE
```

### Creating a view
```
CREATE VIEW CA_CLIENTS AS
   SELECT FirstName, LastName
      FROM CLIENTS
      WHERE CLIENTS.State = 'CA';
```

### Joining two tables as a view
```
CREATE VIEW MALE_CUST AS
   SELECT FirstName, LastName
      FROM CLIENTS JOIN INVOICE
      USING (CustomerID);
```
### Data Definition Language (DDL)
 * **CREATE** - Use to build essential structures of the database including schemas, domains, tables, and views.
 * **ALTER** - Use to change structures that has been created.
 * **DROP** - Use to destroy structures that has been created such as table from a database schema.
 
### Data Manipulation Language (DML)
 * **INSERT**
 * **UPDATE**
 * **DELETE**
 * **MERGE**
 * **SELECT**
 
### Aggregation functions
 * **COUNT** - Returns the number of rows
 ```
 SELECT COUNT (*)
     FROM CLIENTS
     WHERE Age < 35 AND State = 'CA';
 ```

 * **MAX** - Return the maximum value that occurs in the specified column.
 ```
 SELECT FirstName, LastName, Age
     FROM CLIENTS
     WHERE Age = (SELECT MAX(Age) FROM CLIENTS);
 ```
 
 * **MIN** - Opposite of max.
 ```
 SELECT FirstName, LastName, Age
     FROM CLIENTS
     WHERE Age = (SELECT MIN(Age) FROM CLIENTS);
 ```
 
 * **SUM** - Adds up the values in the specified column.
 ```
 SELECT SUM(Age)
     FROM CLIENTS;
 ```
 
 * **AVG** - Return the average of all the value in specified column.
 ```
 SELECT AVG(Age)
     FROM CLIENTS;
 ```
 
