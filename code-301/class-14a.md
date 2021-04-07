# Database Normalization 

Database normalization is a process used to organize a database into tables and columns. The idea is that a table should be about a specific topic and that only those columns which support that topic are included.

There are three main reasons to normalize a database. The first is to minimize duplicate data, the second is to minimize or avoid data modification issues, and the third is to simplify queries. 
(Insertion anomalies, update anomalies, deletion anomalies)

The database community has developed a series of guidelines for ensuring that databases are normalized. These are referred to as normal forms:

-   First Normal Form – The information is stored in a relational table and each column contains atomic values, and there are not repeating groups of columns.
-   Second Normal Form – The table is in first normal form and all the columns depend on the table’s primary key.
-   Third Normal Form – The table is in second normal form and all of its columns are not transitively dependent on the primary key.