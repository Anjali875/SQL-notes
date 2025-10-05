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
