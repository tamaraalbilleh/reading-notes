# Introduction to SQL
its stand for Structured Query Language, and its a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database. And due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications.
## 1: SELECT queries 101

* To retrieve data from a SQL database, we need to write SELECT statements, which are often colloquially refered to as queries.
* A query in itself is just a statement which declares what data we are looking for, where to find it in the database, and optionally, how to transform it before it is returned. 
##  2: Queries with constraints 
* In order to filter certain results from being returned, we need to use a WHERE clause in the query. 
* The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.
* More complex clauses can be constructed by joining numerous AND or OR logical keywords
* writing clauses to constrain the set of rows returned also allows the query to run faster due to the reduction in unnecessary data being returned.
* When writing WHERE clauses with columns containing text data, SQL supports a number of useful operators to do things like case-insensitive string comparison and wildcard pattern matching.

| Operator     | Condition | Example|
| ----------- | ----------- | ----------- |
| = | Case sensitive exact string comparison (notice the single equals) | col_name = "abc" |
| != or <> | Case sensitive exact string inequality comparison | col_name != "abcd" |
| LIKE | Case insensitive exact string comparison | col_name LIKE "ABC" |
| NOT LIKE | Case insensitive exact string inequality comparison | col_name NOT LIKE "ABCD" |
| % | Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE) | col_name LIKE "%AT%"|
| _ | Used anywhere in a string to match a single character (only with LIKE or NOT LIKE) | col_name LIKE "AN_"|
| IN (…)	 | String exists in a list | col_name IN ("A", "B", "C") |
| NOT IN (…) | String does not exist in a list | col_name NOT IN ("D", "E", "F") |
***
* while most database implementations are quite efficient when using these operators, full-text search is best left to dedicated libraries like Apache Lucene or Sphinx. 
* hese libraries are designed specifically to do full text search, and as a result are more efficient and can support a wider variety of search features including internationalization and advanced queries.
## 4: Filtering and sorting Query results
* the DISTINCT keyword will blindly remove duplicate rows
* When an ORDER BY clause is specified, each row is sorted alpha-numerically based on the specified column's value. In some databases, you can also specify a collation to better sort data containing international text.
* The LIMIT will reduce the number of rows to return
* OFFSET will specify where to begin counting the number rows from.
##  13: Inserting rows
* INSERT statement, which declares which table to write into, the columns of data that we are filling, and one or more rows of data to insert. 
* if you have incomplete data and the table contains columns that support default values, you can insert rows with only the columns of data you have by specifying them explicitly.
## 14: Updating rows 
* UPDATE statement : The statement works by taking multiple column/value pairs, and applying those changes to each and every row that satisfies the constraint in the WHERE clause.
*  always write the constraint first and test it in a SELECT query to make sure you are updating the right rows, and only then writing the column/value pairs to update.
## 15: Deleting rows
* a DELETE statement, which describes the table to act on, and the rows of the table to delete through the WHERE clause.
* If you decide to leave out the WHERE constraint, then all rows are removed, which is a quick and easy way to clear out a table completely (if intentional).
## 16: Creating tables
* When you have new entities and relationships to store in your database, you can create a new database table using the CREATE TABLE statement.
* The structure of the new table is defined by its table schema, which defines a series of columns. Each column has a name, the type of data allowed in that column, an optional table constraint on values being inserted, and an optional default value.
* If there already exists a table with the same name, the SQL implementation will usually throw an error
```
CREATE TABLE movies (
    id INTEGER PRIMARY KEY,
    title TEXT,
    director TEXT,
    year INTEGER, 
    length_minutes INTEGER
);
```
## 17: Altering tables
* SQL provides a way for you to update your corresponding tables and database schemas by using the ALTER TABLE statement to add, remove, or modify columns and table constraints.
* when creating new rows in the CREATE TABLE statement. You need to specify the data type of the column along with any potential table constraints and default values to be applied to both existing and new rows.
* Dropping columns is as easy as specifying the column to drop, however, some databases (including SQLite) don't support this feature. Instead you may have to create a new table and migrate the data over.
* If you need to rename the table itself, you can also do that using the RENAME TO clause of the statement.
## 18: Dropping tables
* In some rare cases, you may want to remove an entire table including all of its data and metadata, and to do so, you can use the DROP TABLE statement, which differs from the DELETE statement in that it also removes the table schema from the database entirely.
*  the database may throw an error if the specified table does not exist, and to suppress that error, you can use the IF EXISTS clause
