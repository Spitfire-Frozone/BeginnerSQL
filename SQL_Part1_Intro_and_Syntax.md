# Beginners SQL Part 1 Introduction and Syntax #

## Last Edited: 19-01-2021
-------------------------------------------------------------------------------
## Introduction

Structured Query Language, or SQL is a language used to create and manipulate databases and their entries. The Relational DataBase Management System (RDBMS) is the basis for SQL. In RDBMS the data is stored in database objects called *tables*. A database can contain one or more tables. A table is like any other data table. It has a collection of data entries and consists of columns and rows. However columns are called *fields* and rows are called *records*. A record will contain information from a variety of different attributes. Each field will contain the entire collection of information about a particular attribute. The number of entries in a table is given by the number of records. Terminology I made up now. I will refer to the intersection between fields and records as *domains*. A record will have as many domains as there are fields, but not all domains will have information in them.

## Using SQL in a Website
To build a website that shows data from a database, you will need:

- a RDBMS database program (i.e. MS Access, SQL Server, MySQL)
- to use a scripting language on the server-side, like PHP or ASP
- to use SQL to obtain the data you want to show
- to use HTML / CSS to style the page

# SQL Statements
Databases are navigated using SQL statements. In the most basic form they are sets of commands consisting of keywords, clauses, operators, functions and so on performing actions on tables. Some database systems require a semicolon at the end of each SQL statement, as they allow multiple statements to be executed in a single call to the server. SQL statements can span across multiple lines such that all four statements below are syntaxically valid. 

~~~
SELECT [field(s)] FROM [table]; 

SELECT [field(s)] FROM [table] 

SELECT [field(s)] 
FROM [table]; 

SELECT [field(s)] 
FROM [table]
~~~

Each component of what can appear in a SQL Statement will be outlined below. For details on how to construct SQL statements see SQL_Part2_SQLStatements.md. 

## SQL Keywords
SQL statements include special keywords that allow you to perform a variety of actions on your database. They are not case-sensitive, but it can often help distinguish them from other objects if that are written in capitals.  A list of some of the most important keywords are below. 
<details>
  <summary>Click to expand!</summary>
  
### SELECT
> extracts data from a database
### UPDATE 
> updates data in a database
### DELETE 
> inserts new data into a database
### CREATE DATABASE 
> creates a new database
### ALTER DATABASE 
> modifies a database
### CREATE TABLE 
> creates a new table
### ALTER TABLE 
> modifies a table
### DROP TABLE 
> deletes a table
### CREATE INDEX 
> creates an index (search key)
### DROP INDEX 
> deletes an index

</details>

## SQL Clauses
An SQL clause is used to qualify a keyword, allowing those that only fulfil certain conditions to be obtained. Clauses can also be used to group or order search results. A list of some of more common ones can be seen in the expandable list below. 

<details>
  <summary>Click to expand!</summary>

### WHERE
> filters records such that only those that fulfill a specified condition are extracted
### HAVING
> filters aggregate records (groups) such that only those that fulfill a specified condition are extracted
### ORDER BY
> orders search results
### GROUP BY
> groups records that share the same values into summary rows
### TOP, LIMIT or ROWNUM
> specifies the number of records to return

</details>

## SQL Operators
There are four types of SQL operators. logical operators, arithmetic operators, comparison operators and bitwise operators. 

### Logical Operators
A logical operator is used to further discriminate search results in a clause. Each operator creates a sub-query within the main query and returns all the information that is evaluated to be TRUE if the condition set for the sub-query is fulfilled.

<details>
  <summary>Some examples are:</summary>

### AND 
> a logical AND. Is TRUE if all conditions separated by AND are TRUE
### OR	
> a logical AND. Is TRUE if any of the conditions separated by OR is TRUE	
### NOT	
> Displays a record if the condition(s) is NOT TRUE	


### ALL	 
> is followed by a set of conditions and returns the records (or part of them) that meet all of the conditions specified.	
### ANY 
> is followed by a set of conditions and returns the records (or part of them) that meet at least one of the conditions specified.
### SOME
>  functionally identical to ANY (from what I can gather)


### BETWEEN	
> evaluated to be TRUE if the information in the domain (also referred to an operand is operated on) is within the a specified range of comparisons	
### EXISTS
> evaluated to be TRUE if the subquery returns at least one record	
### IN
> evaluated to be TRUE if the information in a domain (operand) is equal to one of a list of expressions	
### LIKE
> evaluated to be TRUE if the operand matches a pattern	(useful for evaluating strings)


### Symbolic Operators.
This is the generic 
<details>
  <summary>Click to expand!</summary>

### WHERE
> filters records such that only those that fulfill a specified condition are extracted
### HAVING
> filters aggregate records (groups) such that only those that fulfill a specified condition are extracted
### ORDER BY
> orders search results
### GROUP BY
> groups records that share the same values into summary rows
### TOP, LIMIT or ROWNUM
> specifies the number of records to return
