# Beginners SQL Part 2 SQL Keywords and Statements #

## Last Edited: 22-01-2021
-------------------------------------------------------------------------------
## Constructing SQL statements
Now we know what can make up some SQL statements, below I shall detail how to use some of the common keywords.

### SELECT
SELECT is the be-all and end-all of keywords. Most if not all SQL statements that retrive information from a database will start with you selecting some level of information from a table.
~~~
SELECT [field(s)] 
FROM [table]; 
~~~
Multiple fields can be obtained from this statement by using a comma to seperate the required fields. An asterix can be used to obtain all fields.
~~~
SELECT [field_1, field_2] FROM [table]; 

SELECT [*] FROM [table]; 
~~~
If you want only unique entries, the SELECT keyword can be qualified by the keyword DISTINCT, and can be used in the same way as SELECT.
~~~
SELECT DISTINCT [field_1, field_2] FROM [table]; 
~~~
If you want to give a temporary name to a field that only exists for the duration of the query, you can select the data and cast it into an alias using AS.
~~~
SELECT [field] FROM [table] 
AS [field_name]; 
~~~
If you want even more control over this special data, you can create a new table from selected data using SELECT INTO.

### SELECT INTO
SELECT INTO copies data from one table into a new table. It can be used to copy data at a field level, and combined with other keywords to allow copying of particular domains that fulfil some criteria.
~~~
SELECT field_1, field_2, field_3, ...
INTO newtable [IN external_database]
FROM oldtable
WHERE condition;
~~~
The IN clause is there in case the new table needs to be created in a different database to the one that the information is in. 

### INSERT INTO
This means that we neatly segway into another keyword. INSERT (INTO) is used to input data into a table that already exists. You can either enter the data by record, highlighting the fields you want to insert information into and giving their values like so
~~~
INSERT INTO TableName (field_1, field_2, field_3, ...)
VALUES ('value_1', 'value_2', 'value_3', ...);
~~~
However if you plan on making an entry into every domain in a record, the specification of the fields is unnecessary. 
~~~
INSERT INTO TableName 
VALUES ('value_1', 'value_2', 'value_3', ...);
~~~
If the data you want to enter into an existing table comes from another table itself then you can use INSERT INTO SELECT instead. 

### INSERT INTO SELECT
Using this allows for you to copy all or some of the fields from one table to another that already exists. By adding a WHERE clause, you can filter the records in table1 in all fields that will be inserted into table2.
~~~
INSERT INTO table_2 (field_1(table_2), field_2(table_2), field_3(table_2), ...)
SELECT field_1(table_1), field_2(table_1), field_3(table_1), ... [or * if you want them all]
FROM table1
WHERE condition;
~~~

### WHERE
The WHERE condition allows filtering of records by asking if they pass certain requirements

### JOIN

### CASE

## SQL Stored Procedures