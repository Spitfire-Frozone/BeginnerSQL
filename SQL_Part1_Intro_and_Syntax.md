# Beginners SQL Part 1 Introduction and Syntax #

## Last Edited: 19-01-2021
-------------------------------------------------------------------------------
## Introduction

Structured Query Language, or SQL is a language used to create and manipulate databases and their entries. The Relational DataBase Management System (RDBMS) is the basis for SQL. In RDBMS the data is stored in database objects called *tables*. A database can contain one or more tables. A table is like any other data table. It has a collection of data entries and consists of columns and rows. However columns are called *fields* and rows are called *records*. A record will contain information from a variety of different attributes. Each field will contain the entire collection of information about a particular attribute. The number of entries in a table is given by the number of records.

## Using SQL in a Website
To build a website that shows data from a database, you will need:

- a RDBMS database program (i.e. MS Access, SQL Server, MySQL)
- to use a scripting language on the server-side, like PHP or ASP
- to use SQL to obtain the data you want to show
- to use HTML / CSS to style the page

# SQL Statements
Databases are navigated using SQL statements. In the most basic form they are sets of commands consisting of keywords, operators, functions and so on performing actions on tables. Some database systems require a semicolon at the end of each SQL statement, as they allow multiple statements to be executed in a single call to the server. SQL statements can span across multiple lines. Each component of what can appear in a SQL Statement will be outlined below. For details on how to construct SQL statements see SQL_Part2_SQLStatements.md. 

## SQL Keywords
SQL statements include special keywords that allow you to perform a variety of actions on your database. They are not case-sensitive, but it can often help distinguish them from other objects if that are written in capitals.  A list of some of the most important keywords are below. 

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

## SQL Operators
