# Read : 08

## SQL 

- *(pronounced "ess-que-el")* stands for **Structured Query Language**.

- **SQL** is used to communicate with a **database**. According to ANSI *(American National Standards Institute)*, it is the standard language for relational database management systems.


- **What functionalities it cand do?** 
  - Execute queries against a database.
  - Retrieve data from a database.
  - Insert records in a database.
  - Update records in a database.
  - Delete records from a database.
  - Create new databases.
  - Create new tables in a database.
  - Create stored procedures in a database.
  - Create views in a database.
  - Set permissions on tables, procedures, and views.

- There are different versions of the SQL language. However, to be compliant with the ANSI standard, they all support at least the major commands *(such as `**SELECT**`, `**UPDATE**`, `**DELETE**`, `**INSERT**`, `**WHERE**`)* in a similar manner.

- **SQL Commands:**
    - `SELECT` - extracts data from a database.
    - `UPDATE` - updates data in a database.
    - `DELETE` - deletes data from a database.
    - `INSERT INTO` - inserts new data into a database.
    - `CREATE DATABASE` - creates a new database.
    - `ALTER DATABASE` - modifies a database.
    - `CREATE TABLE` - creates a new table.
    - `ALTER TABLE` - modifies a table.
    - `DROP TABLE` - deletes a table.
    - `CREATE INDEX` - creates an index *(search key)*.
    - `DROP INDEX` - deletes an index.

- **Examples:**

```
// SELECT column1, column2, ... FROM table_name; 
SELECT CustomerName, City FROM Customers;
//
// Selecting all columns using *
SELECT * FROM Customers;
//
// UPDATE table_name SET column1 = value1, column2 = value2, ... WHERE condition; 
UPDATE Customers SET ContactName = 'Alfred Schmidt', City= 'Frankfurt' WHERE CustomerID = 1;
//
// DELETE FROM table_name WHERE condition;
DELETE FROM Customers WHERE CustomerName='Alfreds Futterkiste';
//
// INSERT INTO table_name (column1, column2, column3, ...) VALUES (value1, value2, value3, ...); 
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country) VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');
```



##### [Go Back](code_301_reading_notes.md)