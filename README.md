## SELECT STATEMENTS
dump data into database
psql <nameofdatabase> <  file.sql
### Switch to a database
\c <nameofdatabase>
\c employees

1. To see the tables in a database
\dt

<!-- SELECT * FROM <nameofdatabase>  - To see tables  -->

2. To see the object in a specific column 
SELECT <nameofcolumn> FROM <nameofdatabase>
SELECT first_name FROM employees;
SELECT * FROM salaries;


3. Rename a column 
SELECT <nameofcolumn> AS 'new_name';

4. Concatenate columns in a table
*concat() *
SELECT CONCAT(<column_one>, ' '(any string),  <column_two>) AS 'new_column_name' FROM TITLES;
example result 10040is aSenior Engineer

5. SQL FUNCTIONS 
A function is a set of steps that returns a single value
concat()
Types of functions
 - *Aggregate Functions*  - Aggregate functions aggregate data then return a value e.g adding all the salaries in a column and returning the sum
 - *Scalar Functions* - Run against each individual row e.g the concat function concatenates the values in each row as opossed to the entire column and returning  a single value.

 *Aggregate Functions*
 SELECT function(column) FROM nameoftable;
 AVG() - calculates the average of a set of values
 SELECT avg(salary) FROM salaries;
 COUNT() - counts rows in a specified table or view
 MIN() - gets the minimum value in a set of values
 MAX() - get the maximum value in a set of values
 SELECT max(salary) FROM salaries;
 SUM()  - calculates the sum of values
 SELECT sum(salary) FROM salaries;


