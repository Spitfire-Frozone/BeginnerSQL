# Beginners SQL Part 2 SQL Keywords and Statements #

## Last Edited: 19-01-2021
-------------------------------------------------------------------------------
## Introduction
Now we know what can make up some SQL statements, below I shall detail how to use some of the common keywords

### SELECT
> extracts data from a database
~~~
SELECT [field(s)] FROM [table]; 
~~~
Multiple fields can be obtained from this statement by using a comma to seperate the required fields. An asterix can be used to obtain all fields.
~~~
SELECT [field_1, field_2] FROM [table]; 
SELECT [*] FROM [table]; 
~~~
If you want only unique entries, the SELECT keyword can be qualified by the keyword DISTINCT, and cns be used in the same way as SELECT.
~~~
SELECT DISTINCT [field_1, field_2] FROM [table]; 
~~~