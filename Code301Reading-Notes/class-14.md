# Introduction to Database Normalization
Database normalization is a process used to organize a database into tables and columns.  The main idea with this is that a table should be about a specific topic and only supporting topics included.
where the data contains salespeople and customers serving several purposes:
* Identify salespeople in your organization
* List all customers your company calls upon to sell a product
* Identify which salespeople call on specific customers.
## Reasons for Database Normalization
There are three main reasons to normalize a database.  The first is to minimize duplicate data, the second is to minimize or avoid data modification issues, and the third is to simplify queries. 
## Data Duplication and Modification Anomalies
Notice that for each SalesPerson we have listed both the SalesOffice and OfficeNumber. There are duplicate salesperson data. Duplicated information presents two problems:

It increases storage and decrease performance.
It becomes more difficult to maintain data changes.
### Insert Anomaly
There are facts we cannot record until we know information for the entire row. 
### Update Anomaly
In this case we have the same information in several rows.

## Search and Sort Issues
The last reason we’ll consider is making it easier to search and sort your data. 

summarize the various forms:

* First Normal Form – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
* Second Normal Form – The table is in first normal form and all the columns depend on the table’s primary key.
* Third Normal Form – the table is in second normal form and all of its columns are not transitively dependent on the primary key
