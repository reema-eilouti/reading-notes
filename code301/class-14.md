# Read : 14

## DB Normalization

- Database normalization is a process used to organize a database into tables and columns.

- A table should be about a specific topic and only supporting topics included. 

- DB Normalization is used to reduce the number of duplicate data contained within the database, which eliminates some issues stemming from database modifications. 

- Duplicated information presents two problems:
    1. It increases storage and decrease performance.
    2. It becomes more difficult to maintain data changes.

- **Reasons for Database Normalization**: *The first* is to **minimize duplicate data**, *the second* is to **minimize or avoid data modification issues**, and *the third* is to **simplify queries**.  

- **Modification Anomalies** are issues that arise when we modify the database, abnormalities and inconsistency.

- There are three modification anomalies that can occur:
    1. **Insert Anomaly.**
        - the inability to add data to the database due to the absence of other data
    2. **Update Anomaly.**
        - a data inconsistency that results from data redundancy and a partial update
    3. **Deletion Anomaly.**
        - when you delete a record that may contain attributes that shouldn't be deleted


- There are three common forms of **database normalization:** *1st, 2nd, and 3rd* normal form. 
- They are also abbreviated as **1NF, 2NF, and 3NF** respectively. 

1. **First Normal Form –** The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.

2. **Second Normal Form –** The table is in first normal form and all the columns depend on the table’s primary key.

3. **Third Normal Form –** the table is in second normal form and all of its columns are not transitively dependent on the primary key.

##### [Go Back](code_301_reading_notes.md)