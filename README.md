# SQL-notes:
Database is a collection of related information (eg:phone book, todo list, shopping list, etc) which can be stored in diff. ways (on a computer, on paper, etc).
DBMS is a special software that helps users create and maintain a database. it handles large amounts of information, security, backups, importing-exporting data, etc.
CRUD represents the 4 main operations done with the database. they're create, read, update, delete.
A schema is the blueprint or structure of a database. It defines how the data is organized — what tables exist, what columns they have, what data types, and how tables are related.
2 types of databases: Relational Databases(SQL) and non-relational(Non-SQL)
relational databases organise data into one or more tables whereas, non-relational doenst use tables.
Relational: each table has rows and columns. Each table is related to other tables through keys
Non-relational: It is more flexible, handling unstructured or semi-structured data such as JSON, key-value pairs, documents, or graphs.
Relational Database Management Systems (RDBMS):
Help users create and maintain a relational database
mySQL, Oracle, postgreSQL, mariaDB, etc.
Structured Query Language (SQL):
Standardized language for interacting with RDBMS
Used to to perform C.R.U.D operations, as well as other administrative tasks (user management, security, backup, etc).
Used to define tables and structures
SQL code used on one RDBMS is not always portable to another without modification.
Non-Relational Database Management Systems (NRDBMS): Help users create and maintain a non-relational database
mongoDB, dynamoDB, apache cassandra, firebase, etc
Implementation Specific:
Any non-relational database falls under this category, so there's no set language standard.
Most NRDBMS will implement their own language for performing C.R.U.D and administrative operations on the database.
Queries are requests made to the database management system for specific information
As the database's structure become more and more complex, it becomes more difficult to get the specific pieces of information we want.
eg: A google search is a query
Keys are used to uniquely identify and link records in a table.
They maintain data integrity and prevent duplicate or invalid data.
Types of Keys:
1) Primary Key-
Uniquely identifies each record in a table.
Cannot be NULL and cannot have duplicates.
Each table can have only one Primary Key.
2) Foreign Key-
Used to link two tables together.
It refers to the Primary Key in another table.
Maintains referential integrity (prevents orphan data).
Structured Query Language (SQL):
SQL is a language used for interacting with Relational Database Management Systems (RDBMS). You can use SQL to get the RDBMS to do things for you like:
Create, retrieve, update & delete data
Create & manage databases
Design & create database tables
Perform administration tasks (security, user management, import/export, etc
SQL is actually a hybrid language, it's basically 4 types of languages in one
*Data Query Language (DQL):Used to query the database for information.
Get information that is already stored there
*Data Definition Language (DDL): Used for defining database schemas.
*Data Control Language (DCL):Used for controlling access to the data in the database.
User & permissions management
*Data Manipulation Language (DML): used for inserting, updating and deleting data from database.
A query is a set of instructions given to the RDBMS that tells the RDBMS what information you want it to retrieve for you: tons of data in a DB often hidden in a complex schema goal is to only get the data you need.
Using MySQL and PopSQL:
To connect, configuration details like host, port, and user credentials are required. -MySQL is a strong and reliable RDBMS. -PopSQL is a query editor that simplifies writing and executing queries with instant results. -Setting up a local MySQL server involves installation, configuration, and creating users. 
Creating and Modifying Tables -Core SQL data types: INT, VARCHAR, DATE. -CREATE TABLE defines a new table structure. -Syntax and semicolon usage must be correct. -ALTER TABLE allows adding or dropping columns after creation. 
Inserting Data and Constraints -Schema must be created before inserting data. -INSERT INTO statement is used with VALUES to add rows. -Constraints ensure data integrity: 
NOT NULL → column cannot be empty. 
UNIQUE → no duplicate values allowed. -Default values can be set to simplify data entry (e.g., major = ‘undecided’). 
AUTO_INCREMENT and Data Updates:
-AUTO_INCREMENT automatically assigns sequential values to primary keys. -Makes inserting data easier (no need to manually set IDs). -Constraints ensure only valid data is stored. -UPDATE → modify existing data. -DELETE → remove records. 
Ordering and Filtering Data:
-ORDER BY sorts results based on column values (e.g., salary, student ID). -LIMIT restricts number of results returned. -WHERE filters results based on conditions. 
Complex Schema Design:
-Example schema: employees, branches, and clients. -Relationships defined using foreign keys
Querying Data -SELECT retrieves information from tables. -ORDER BY sorts output. -Aggregation functions summarize data: 
COUNT → counts rows. 
AVG → calculates averages. 
SUM, MIN, MAX also commonly used. 
Wildcards and Pattern Matching -LIKE operator allows pattern-based searches. -% → matches any number of characters. - _ → matches a single character. - Useful for names, partial matches, or date searches. 
Combining Data: UNION and JOIN -UNION combines results of two SELECT queries (same number of columns, same data types)             -JOIN merges rows from different tables using common columns. - Types of JOIN: 
INNER JOIN → only matching rows. 
LEFT JOIN → all from left table + matches. 
RIGHT JOIN → all from right table + matches. 
Nested Queries and Trigger -Nested queries use one query as input for another. -IN keyword filters results from subqueries. -Handling deletions: 
ON DELETE SET NULL → replaces deleted value with NULL. 
ON DELETE CASCADE → deletes related rows automatically.
-Triggers = predefined SQL code executed on events like INSERT, UPDATE, DELETE. 
Triggers in MySQL -Triggers automate tasks and maintain consistency. 
-Must change SQL delimiter when creating them. -Can include conditions (IF statements). -Common uses: logging, validations, enforcing rules. 
Data Modeling and Attributes -Single attribute → only one value (e.g., GPA). -Multi-valued attribute → multiple values (e.g., clubs a student belongs to). -Derived attribute → calculated from other attributes (e.g., honors from GPA). -ER diagrams show relationships and participation: 
Total participation → all entities involved. 
Partial participation → only some entities involved. 
ER Diagram Example (Company Database) -Employee–Branch relationship: 
One branch → many employees. 
Employee works for one branch. -Every branch must have a manager (full participation). -Not every employee is a manager (partial participation). -Supervision: one employee supervises many but reports to one. -Client–Branch: every client belongs to a branch, but not every branch has clients. 
Mapping ER Diagrams to Schemas -Conversion involves systematic steps. -Foreign keys and relationships must be clearly defined. -Arrows can show table relationships but may complicate diagrams. -ER diagrams help convert requirements into working schemas. -Practice improves database design skill
