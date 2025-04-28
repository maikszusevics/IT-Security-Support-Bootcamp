# SQL Intro - W3Schools


## Objective

To build a foundational understanding of SQL queries and syntax in preparation for IT support and security roles.

### Key Concepts Learned

- SQL keywords are not case sensitive: `select` is the same as `SELECT`
- Semicolon is the standard way to separate each SQL statement in database systems that allow more than one SQL statement to be executed in the same command.
- ##### Important SQL Commands:
	- `SELECT` - extracts data from a database
	- `UPDATE` - updates data in a database
	- `DELETE` - deletes data from a database 
	- `INSERT INTO` - inserts new data into a database
	- `CREATE DATABASE` - creates a new database
	- `ALTER DATABASE` - modifies a database
	- `CREATE TABLE` - creates a new table
	- `ALTER TABLE` - modifies a table
	- `DROP TABLE` - deletes a table
	- `CREATE INDEX` - creates an index (search key)
	- `DROP INDEX` - deletes an index
- ##### Important SQL Syntax:
	- `*` means "all columns"
	- `AND` is a boolean operator in SQL, a logical "both must be true" test. If you have `Condition1 AND Condition2`, a row only passes this test when **both** conditions are true.
	- `OR` is a another boolean operator in SQL, it is used to retrieve results where at least one of the specified conditions are met
	- `,` commas are used to list, for example: 
		- if you are specifying two specific columns you would separate them by a comma: `SELECT first_name, last_name, email FROM customers;`
		- if you are inserting multiple values into a table at once you would separate them by a comma: `INSERT INTO products (name, price, category) VALUES ('Laptop', 999.99, 'Electronics');`
		- if you are creating a table you would separate the name and data type of each column by a comma: `CREATE TABLE users (id INT, username VARCHAR(50), join_date DATE);`
	- `DISTINCT` is used to eliminate duplicate rows under the same column 
	- `WHERE` is used to filter records based on specified conditions
	- `COUNT` will return the number of rows in a specified column
	- `ORDER BY` is used to order results in ascending (`ASC`) or descending (`DESC`) order. Uses Ascending order if not specified.
	- `LIKE` is used to find data entries which have specific data, like starting with a specific character (i.e `LIKE 'G%'` will select all rows under that column which have data entries starting with G)
	- `%` is a character that represents zero, one, or multiple characters

---


### Practical Examples


```
# How would you select everything in the customers table?

SELECT * FROM CUSTOMERS;

# How would you select the "CustomerName" and "City" columns from a table named "Customers"?

SELECT CustmomerName, City FROM Customers; 

# How would you select the number of different countries in the Countries column?

SELECT COUNT(DISTINCT Countries) FROM Customers;

# How would you select all customers from Mexico?

SELECT * FROM Customers WHERE Country="mexico";

# How would you sort all products by price?

SELECT * FROM Products ORDER BY Price DESC;

# How would you select all customers from Latvia whose names start with "M"?

SELECT * FROM Customers WHERE Country = "Latvia" AND CustomerName LIKE "M%";

# How would you select all customers that are not from Riga or London

SELECT * FROM Customers WHERE NOT (City = "Riga" OR City = "London");

```

#### Reflection 

Learning SQL queries and syntax equips me with tools needed to diagnose and support database-related issues. This is greatly helping to prepare me to confidently contribute in support and security environments. [W3Schools](https://www.w3schools.com/sql/sql_syntax.asp) has made these foundational concepts easy to grasp and apply. 