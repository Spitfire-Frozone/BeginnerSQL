# Beginners SQL Part 1 Introduction and Syntax #

## Last Edited: 22-01-2021
-------------------------------------------------------------------------------
## Introduction

Structured Query Language, or SQL is a language used to create and manipulate databases and their entries. The Relational DataBase Management System (RDBMS) is the basis for SQL. In RDBMS the data is stored in database objects called *tables*. A database can contain one or more tables. A table is like any other data table. It has a collection of data entries and consists of columns and rows. However columns are called *fields* and rows are called *records*. A record will contain information from a variety of different attributes. Each field will contain the entire collection of information about a particular attribute. The number of entries in a table is given by the number of records. Terminology I made up now. I will refer to the intersection between fields and records as *domains*. A record will have as many domains as there are fields, but not all domains will have information in them.

## Website-Based SQL
To build a website that shows data from a database, you will need:

- a RDBMS database program (i.e. MS Access, SQL Server, MySQL)
- to use a scripting language on the server-side, like PHP or ASP
- to use SQL to obtain the data you want to show
- to use HTML / CSS to style the page

## General Syntax Points
:closed_book: Comments are made with two dashed lines -- 

:green_book: Domains that are empty can be identifies and manipulated by using the NULL keyword 

:blue_book: If you want to make code easy to read, you might want to rename tables or records. These can be done by assigning them an alias for the duration of your query. 

:orange_book: SQL wildcards are special characters used to replace parts of a string. These are useful for searches. These are different depending on what you are using to code SQL. 

| Symbol     |           | Description                                    | Example                                                                                                                                |
|------------|-----------|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| SQL Server | MS Access |                                                |                                                                                                                                        |
|      *     |     %     | Represents zero or more characters             | ma* => ma, map, magaluf69, ... <br>m*p => mp, map, m1shap, ...<br><br>ma% => ma, map, magaluf69, ... <br>m%p => mp, map, m1shap, ...   |
|      ?     |     _     | Represents a single character                  | m?p => map, mbp ... m0p, ...  <br>??mp => camp, bump, 80mp, ...<br><br>m_p => map, mbp ... m0p, ...  <br>__mp => camp, bump, 80mp, ... |
|     []     |     []    | Represents any one character in these brackets | m[ao]p => map, mop<br>[bc][au]mp => bamp, bump, camp, cump                                                                             |
|     [!]    |    [^]    | Represents any character not in the brackets   | m[^bcdefghijklmnopqrstuvwxyz1234567890]p = map <br>m[!bcdefghijklmnopqrstuvwxyz1234567890]p = map                               |
|      -     |     -     | Represents a range of characters               | m[a-f]p => map, mbp, mcp, mdp, mep, mfp <br>m[0-5]p => m0p, m1p, m2p, m3p, m4p, m5p                                                    |
|      #     |           | Represents any numeric character               | 12# => 120 - 129 <br>12## => 1200 - 1299                                                                                               |                                                                   |


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
> deletes data from a database
### CREATE DATABASE 
> creates a new database
### ALTER DATABASE 
> modifies a database
### CREATE TABLE 
> creates a new table
### SELECT INTO
> creates a new table with information from the selected table
### INSERT INTO
> inserts new records into a table 
### INSERT INTO SELECT
>  copies data from a table and inserts it into an existing table
### ALTER TABLE 
> modifies a table
### DROP TABLE 
> deletes a table
### CREATE INDEX 
> creates an index (search key)
### DROP INDEX 
> deletes an index
### CASE
> allows multiple conditions to be tested sequentially outputting a value when the first condition it comes across is true. It uses a WHEN-THEN-ELSE which is akin to IF-THEN-ELSE structures in other languages. 

</details>

## SQL Clauses
An SQL clause is used to qualify a keyword, allowing those that only fulfil certain conditions to be obtained. Clauses can also be used to group or order search results. A list of some of more common ones can be seen in the expandable list below. 

<details>
  <summary>Click to expand!</summary>

### AS
> stores extracted or manipulated data from the database as something else.
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
### JOIN
> combines rows from two or more different tables, based on a related column between them. There are 5 types of join.
### ON 
> specifies the target of a join 

</details>

## SQL Operators
There are four types of SQL operators: logical operators, arithmetic operators, comparison operators and bitwise operators. 

### Logical Operators
A logical operator is used to further discriminate search results in a clause. Each operator creates a sub-query within the main query and returns all the information that is evaluated to be TRUE if the condition set for the sub-query is fulfilled.

<details>
  <summary>Click to expand for some examples!</summary>

### AND 
> a logical AND. Is TRUE if all conditions separated by AND are TRUE
### OR	
> a logical AND. Is TRUE if any of the conditions separated by OR is TRUE	
### NOT	
> Displays a record if the condition(s) is NOT TRUE	
### UNION
> combines the results from multiple SELECT statements

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

</details>

### Comparison Operators.
Does what it says on the tin. These are the set of operators that allow you to compare domains. You are already familiar most of these 
<details>
  <summary>Click to expand for some examples!</summary>

#### =	Equal to	
#### >	Greater than	
#### <	Less than	
#### >=	Greater than or equal to	
#### <=	Less than or equal to	
#### <>	Not equal to

</details>

### Arithmetic Operators.
SQL can be used to do simple arithmetic, and for that the operators you would normally use for simple sums are used here. There is a catch. Since SQL doesn't have an express type attribute for items returned values may not be correct (this is mainly only a concern if the division operator is being used). If the input is all integers for example, it will always output an integer and any remainders will be discarded. Since SQL automatically detects number types, a float can always be specified by entering a number with a decimal point. i.e 30.0 instead of 30. If any one of the numbers in a calculation is a float, however, the a answer will be a float.

<details>
  <summary>Click to expand for some examples!</summary>

### +	Add	
### -	Subtract	
### *	Multiply	
### /	Divide	
> Divides two numbers together but retains the variable type. 
### %	Modulo
> When A % B. The modulo operation prints the remainder when B divides into A. This is only reliable for integers. If floats are input, they are rounded down to the nearest integer before the calculation is done. 

</details>

### Bitwise Operators.
These are rarely used as it's not often that individual bits want to be manipulated, maybe you are using some legacy code> An example could be if you wanted to check individual bits in a binary or a hexidecimal number. These operators mostly fail when used on decimal numbers. The concatination operator is the most useful one of these and is nothing like the rest. 

<details>
  <summary>Click to expand for some examples!</summary>

### & - bitwise AND
> 
### | - bitwise OR
> 
### ^ or # - bitwise exculsive OR (XOR)
>
### ~ - bitwise NOT
>
### || - concatination 
> combines by appending multiple fields together. Usually to make a new field from multiple strings.  
~~~
SELECT [field1] || '[####]' || [field2] AS [newfield]
~~~
> The central part of this operation allows user inputs to the new text. Here you can add any string you want including just a space. The AS part allows this to be saved for further manipulation.

</details>

:snowboarder: Most of the symbolic operations that make up the latter two catagories can be appended by an equals sign to create a *compound* operator. A compound operator is very useful for quickly accessing domains and editing the information within. 

## SQL Functions
An SQL function is a quick way of doing calculations with fields, they take a given field as an argument and output some value.    

<details>
  <summary>Click to expand for some examples!</summary>

### MIN(field)
> returns the minimum value in the selected field

### MAX(field)
> returns the maximum value in the selected field

### COUNT(field/criterion)
> return the number of records that filfil certain criteria, or the number of entries in a given field

### AVG(numeric_field)
> returns the mean value of a field consting of numbers 

### SUM(numeric_field)
> returns the sum of all of the values in a numeric field

### ISNULL(field, [value]), IFNULL(field, [value])
> checks if a domain is empty, and if so replaces it in a calculation with [value]

### COALESCE(field)
> reads items in a field iteratively and returns the first non-null value

</details>