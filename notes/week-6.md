# Week 6 Notes
SQL Basics**

SQL is the language you use to talk to a database. It helps you pull out the information you need, add new data, and organize everything in a clear, structured way. Once you understand these core commands, you can work with almost any relational database.

## **Retrieving Data with SELECT**

The SELECT statement is your main tool for asking the database questions. You use it when you want to view information stored in a table.

If you want to see only one column, for example the name of every customer, you can write:

```
SELECT name FROM customers
```

You can request more than one column at a time. For instance, if you want names and emails:

```
SELECT name, email FROM customers
```

If you want to see everything the table contains, every column and every row, you can simply write:

```
SELECT * FROM customers
```

You can also filter your results so you only get the information that matters to you. For example, to see customers older than eighteen:

```
SELECT name FROM customers WHERE age > 18
```

There are many ways to filter results. You can match specific text, search between a range of numbers, or even check for patterns such as emails that end with gmail:

```
WHERE city = 'London'
WHERE age BETWEEN 18 AND 30
WHERE email LIKE '%gmail.com'
```

Filters are powerful because they allow you to narrow down large amounts of data to exactly what you need.

## **Adding New Rows with INSERT**

INSERT is the command that lets you add new information to a table.

To insert a single customer into your database:

```
INSERT INTO customers (name, email)
VALUES ('John', 'john@email.com')
```

You can add more than one row at the same time. This is not only cleaner but more efficient:

```
INSERT INTO customers (name, email)
VALUES ('Sarah', 'sarah@email.com'),
       ('Mike', 'mike@email.com')
```

It is always a good idea to include the list of column names when inserting data because it prevents mistakes if the table structure changes later on.

## **Using Functions for Math and Text**

SQL includes built-in functions that help you analyze and clean up your data.

Math and aggregate functions work across multiple rows. They help you count, add, average, and identify important values:

COUNT gives you the total number of rows
SUM adds up a numeric column
AVG calculates the average value
MAX finds the highest number
MIN finds the lowest number

For example, if you want to see how many orders you have:

```
SELECT COUNT(*) FROM orders
```

There are also functions for text formatting. These are helpful when you need to clean up inconsistent text or create readable output:

UPPER turns text into capital letters
LOWER makes everything lowercase
CONCAT joins pieces of text together

If you want to turn someone’s first and last name into a single full name:

```
SELECT CONCAT(first_name, ' ', last_name) AS full_name FROM users
```

## **Sorting and Grouping Your Results**

Sorting your results makes the data easier to interpret. You can sort from lowest to highest or from highest to lowest. For example, to arrange your products by price from the cheapest to the most expensive:

```
SELECT * FROM products ORDER BY price ASC
```

Sorting is especially useful when reviewing reports, comparing values, or checking trends.

