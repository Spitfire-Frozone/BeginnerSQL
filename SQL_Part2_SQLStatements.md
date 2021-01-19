# Beginners SQL Part 2 SQL Keywords and Statements #

## Last Edited: 19-01-2021
-------------------------------------------------------------------------------
## Constructing SQL statements
Now we know what can make up some SQL statements, below I shall detail how to use some of the common keywords.

### SELECT
Select is the be-all and end-all of keywords. Most if not all SQL statements that retrive information from a database will start with you selecting some level of information from a table.
~~~
SELECT [field(s)] 
FROM [table]; 
~~~
Multiple fields can be obtained from this statement by using a comma to seperate the required fields. An asterix can be used to obtain all fields.
~~~
SELECT [field_1, field_2] 
FROM [table]; 

SELECT [*] 
FROM [table]; 
~~~
If you want only unique entries, the SELECT keyword can be qualified by the keyword DISTINCT, and can be used in the same way as SELECT.
~~~
SELECT DISTINCT [field_1, field_2] FROM [table]; 
~~~