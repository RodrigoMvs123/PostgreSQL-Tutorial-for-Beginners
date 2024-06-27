
## PostgreSQL-Tutorial-for-Beginners

https://www.youtube.com/watch?v=SpfIwlAYaKk 

https://raw.githubusercontent.com/RodrigoMvs123/PostgreSQL-Tutorial-for-Beginners/main/README.md

https://github.com/RodrigoMvs123/PostgreSQL-Tutorial-for-Beginners/blame/main/README.md

## Step 1 
Download and install PostgreSQL 

- https://www.postgresql.org/ 

Download 

Windows

- https://www.postgresql.org/download/windows/ 

Download the installer 

Windows x86-64

## Step 2
Download and Install PgAdmin 

- https://www.pgadmin.org/download/pgadmin-4-windows/ 
pgAdmin4v74 ( released June 29, 2023 )

Files

pgadmin-7.4-x64.exe

## Step 3 
Download ( but do not directly open ) dvdrental.tar 

file 

- https://www.postgresqltutorial.com/postgresql-getting-started/postgresql-sample-database/ 


Download Supplemental Resources 


Course content

23 Variables / Resources

HTML_NEXT_STEPS_CODE.zip

https://business-support.udemy.com/hc/en-us/articles/115005537648--Downloading-Supplemental-Resources#:~:text=If%20a%20lecture%20has%20resources,clicking%20on%20the%20resource's%20title. 

## step 4 
Restart your computer 

## Step 5
Restore the Database ( ignore failed Exit Code if it appears ) 

```
Open
pgAdmin 4 
Run as Administrator 
Control Panel
Programs 
Uninstall a Program
PostgreSQL 15
Individual Components 
pgAdmin 4
pgAdmin 4v7
Run as Administrator 
```

```
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
Connect to server
Ok
```

```
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
Databases / Create / Database / dvdrental
postgres
dvdrental ( Restore ) 
File Name / All Files / Downloads / dvdrental
Restore
localhost:5432
```

dvdrental ( Query Tool ) 

## Query 
```
SELECT * FROM film;
```
```
Data Output 
film_id     title      description 
…            …         …
```

```
SELECT column_name FROM table_name 
```
```
Database 
Table 1    Table 2     Table 3 
…            …              …
```

```
SELECT c1 FROM table_1
SELECT c1, c2 FROM table_1 
SELECT c1, c2 FROM table_3
SELECT * FROM table_1
```

```
Open
pgAdmin 4 v7
Run as Administrator 
```

```
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
Schemas
Public 
Tables
``` 

## Query
```
SELECT * FROM actor;
```
```
Data Output 
…
```

```
Open
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
Schemas
Public 
Tables
Actor
Columns 
```

## Query
```
SELECT first_name FROM actor;
```
```
Data Output 
first_name 
…
```

```
Open 
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
Schemas
Public 
Tables
Actor
Columns 
```

## Query
```
SELECT first_name, last_name FROM actor;
```
```
Data Output 
first_name      last_name 
…                   …
```

```
SELECT Challenges Tasks
Challenges Structures 
Business Situation 
Challenge Question
Expected Answer
Hints
Solution 
```

#### Situation 

We want to see the payment of ours existing customers 

#### Challenge 

Use a SELECT statement to grab the customer id of every customer the payment date and the amount 

```
Data Output 
customer_id     amount        payment_date
…                     …                …
```

#### Hints 
User the payment table> You can use the table to drop-down to view what columns are available 

#### Solution 
Let´s open pgadmin

```

Open
pgAdmin 4
Object Explorer
Servers
dvdrental
Query Tool 
Tables 
Payment 
Columns 
```

## Query 
```
SELECT customer_id, amount, payment_date FROM payment;
```
```
Data Output 
customer_id     amount        payment_date
…                     …                …
```

```
SELECT DISTINCT 
```
```
SELECT DISTINCT column FROM table_name;
```
```
SELECT DISTINCT first_name, last_name FROM employees 
```
```
Data Output 
first_name     last_name
…                  …
```

```
Open
pgAdmin 4
Object Explorer
Servers
dvdrental
Query Tool 
```

## Query 
```
SELECT * FROM film;
```

```
Open
pgAdmin 4
Object Explorer
Servers
dvdrental
Schema
public
Tables 
film
Columns 
```

```
Data Output
film_id    title    description    … 
…           …      …                  …
```

## Query
```
SELECT DISTINCT release_year FROM film;
```

```
Data Output 
release_year
…
```

## Query 
```
SELECT * FROM film;
```

```
Data Output 
film_id      title    description     ….
….            …     …
```

## Query 
```
SELECT rental_rate from film;
```

```
Data Output 
rental_rate 
…
```

## Query 
```
SELECT DISTINCT rental_rate from film;
```

```
Data Output 
rental_rate 
…
```

## Query 
```
SELECT DISTINCT first_name
FROM customer;
```

```
Data Output 
first_name 
…
```

Count 

## Query
```
SELECT COUNT(*) FROM employees;
```

```
Data Output 
Count
5 
```

## Query 
```
SELECT COUNT ( DISTINCT Department )
FROM employees;
```

```
Data Output 
Count 
3
```

## Query 
```
SELECT COUNT(*) FROM table_name;
```

## Query 
```
SELECT COUNT (student_name) FROM students;
```

## Query 
```
SELECT COUNT (student_name) 
FROM table_name;
```

```
Data Output
Count 
4 
```

```
Open
pgAdmin 4
Object Explorer
Servers
dvdrental
Query Tool
Schema
public
Tables 
payment
```

## Query
```
SELECT * FROM payment;
```

```
Data Output 
payment_id   customer_id staff_id …
```

## Query
```
SELECT COUNT(*) FROM payments;
```
```
Data Output
Count
14596
```

## Query
```
SELECT COUNT(amount) FROM payments;
```
```
Data Output
Count
14596
```

## Query
```
SELECT DISTINCT amount FROM payment;
```
```
Data Output
amount
11   5.99
..
```

## Query
```
SELECT COUNT (DISTINCT amount) FROM payments;
```
```
Data Output
Count
1   19
```

## Query
```
SELECT COUNT (DISTINCT (amount)) FROM payments;
```
```
Data Output
Count
1   19
```

```
SELECT WHERE

SELECT column1, column2,…
   FROM table_name
   WHERE condition;
```

## Query 
```
SELECT * FROM Employees
WHERE department = ‘Sales’;
```

# Data Output
```
employee_id first_name  last_name  job_title      age  salary     department experience 
5                   Michael       Brown        Supervisor 32     650000  Sales          8                   
rating  phone_number
4.3      555-777-8888
```

## Query 
```
SELECT * FROM Employees
WHERE department <> ‘Finance’; ( It will select the department that is not the Finance department ) 
```

## Query 
```
SELECT * FROM Employees
WHERE age > 30;
```

## Query 
```
SELECT * FROM Employees
WHERE salary < 50000;
```

## Query 
```
SELECT * FROM Employees
WHERE experience >= 5;
```

## Query 
```
SELECT * FROM Employees
WHERE rating <= 4.5;
```
## Query 
```
SELECT * FROM Employees
WHERE age BETWEEN 25 AND 40;
```

## Query 
```
SELECT * FROM Employees
WHERE first_name LIKE ‘J%’;
```

## Query 
```
SELECT * FROM Employees
WHERE department IN (‘HR’, ‘Finance’, ‘Admin’);
```

## Query 
```
SELECT * FROM Employees
WHERE phone_number IS NULL;
```

## Query 
```
SELECT * FROM Employees
WHERE department = (‘HR’ AND age >= 30;
```

## Query 
```
SELECT * FROM Employees
WHERE department = ‘Finance’ OR department = ‘Marketing’;
```

```
Open
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
dvdrental
Query Tool
Schema
public
Tables 
customer 
Columns
```

## Query 
```
SELECT * FROM customer;
```
```
Data Output 
customer_id   store_id    first_name   …
…                   …             …                 …
```

## Query 
```
SELECT * FROM customer WHERE first_name = ‘Mary’;
customer_id   store_id    first_name   …
…                   …             Mary            …
```

```
Open
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
dvdrental
Query Tool
Schema
public
Tables 
film 
Columns
```

## Query
```
SELECT * FROM film;
```
```
Data Output
film_id   title   description …
…          …      …              …
```

## Query
```
SELECT * FROM film WHERE rental_rate > 4;
```
```
Data Output
film_id   title   description …  rental_rate …
…          …      …              …  4.99          …
```

## Query
```
SELECT * FROM film WHERE rental_rate > 4 and replacement_cost >= 19.99;
```
```
Data Output
film_id   title   description …  rental_rate … replacement_cost   …
…          …      …              …  4.99          …  19.99                      …
```

## Query
```
SELECT * FROM film WHERE rental_rate > 4 and replacement_cost >= 19.99;
AND rating = ‘R’;
```
```
Data Output
film_id   title   description …  rental_rate … replacement_cost   … rating …
…          …      …              …  4.99          …  19.99                      … R        …
```

## Query
```
SELECT COUNT(*) FROM film WHERE rental_rate > 4 and replacement_cost >= 19.99;
AND rating = ‘R’;
```
```
Data Output
Count
34
```
## Query
```
SELECT COUNT(title) FROM film WHERE rental_rate > 4 and replacement_cost >= 19.99;
AND rating = ‘R’;
```
```
Data Output
Count
34
```

## Query 
```
SELECT * FROM film;
```
```
Data Output
film_id   title   description …
…          …     …
```

## Query 
```
SELECT * FROM film WHERE rating = ‘R’ OR rating = ‘PG-13’
```
```
Data Output
film_id   title   description …
…          …     …
```

## Query 
```
SELECT COUNT(*) FROM film WHERE rating = ‘R’ OR rating = ‘PG-13’
```
```
Data Output
film_id   title   description …
…          …     …
```

```
SELECT WHERE

SELECT title, replacement_cost FROM film
WHERE release_year >= 2000 AND rating = ‘PG-13’;

SELECT title 
WHERE rating = ‘PG’ AND replacement_cost = 10.99;

SELECT title FROM film
WHERE release_year < 2000 OR replacement_cost < 10;
```

COUNT

```
SELECT COUNT(*) FROM employees;
```
```
Data Output 
Count
5
```

## Query 
```
SELECT COUNT (DISTINCT department) 
FROM employees;
```
```
Data Output 
Count
3
```
```
SELECT COUNT(*) FROM table_name;

SELECT COUNT (student_name) FROM students;

SELECT COUNT (student_name) 
FROM table_name;
```
```
Data Output
Count
4
```

```
Open
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
dvdrental
Query Tool
Schema
public
Tables 
payment
```

## Query
```
SELECT * FROM payment;
```
```
Data Output
payment_id   customer_id   staff_id   …
…                  …                    …           …
```

## Query
```
SELECT COUNT(*) FROM payment;
```
```
Data Output
count
14956
```

## Query
```
SELECT COUNT(amount) FROM payment;
```
```
Data Output
count
14956
``` 

## Query
```
SELECT DISTINCT amount FROM payment;
```
```
Data Output
amount
5.99
…
```

## Query
```
SELECT COUNT (DISTINCT (amount)) FROM payment;
```
```
Data Output
count
19
```

ORDER BY

```
SELECT column1, column2,...
FROM table_name
WHERE conditions
ORDER BY column1 [ASC|DESC], column2[ASC|DESC],...;
```

```
Open
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
dvdrental
Query Tool
Schema
public
Tables 
customer
```

## Query 
```
SELECT * FROM customer;
```
```
Data Output
payment_id   store_id   first_name   …
…                  …                    …           …
```

## Query 
```
SELECT * FROM customer ORDER BY first_name;
```
```
Data Output
payment_id   store_id   first_name   …
…                  …                    …           …
```

## Query 
SELECT * FROM customer ORDER BY first_name ASC;

Data Output
payment_id   store_id   first_name   …
…                  …                    …           …

Query 
SELECT * FROM customer ORDER BY first_name DESC;

Data Output
payment_id   store_id   first_name   …
…                  …                    …           …

Query 
SELECT * FROM customer ORDER BY store_id;

Data Output
payment_id   store_id   first_name   …
…                  …                    …           …

Query 
```
SELECT * FROM customer ORDER BY store_id, first_name;
```
```
Data Output
payment_id   store_id   first_name   …
…                  …                    …           …
```

## Query 
```
SELECT * store_id, first_name, last_name FROM 
customer ORDER BY store_id;
```
```
Data Output
store_id   first_name   last_name
…                    …           …
```
## Query 
```
SELECT * store_id, first_name, last_name FROM 
customer ORDER BY store_id ASC, first_name DESC;
```
```
Data Output
store_id   first_name   last_name
…                    …           …
```

## Query 
```
SELECT * store_id, first_name, last_name FROM 
ORDER BY store_id ASC, first_name ASC;
```
```
Data Output
store_id   first_name   last_name
…                    …           …
```

## Query 
```
SELECT * first_name, last_name FROM 
ORDER BY store_id ASC, first_name ASC;
```
```
Data Output
first_name   last_name
…                …
```

LIMIT

```
SELECT column1, column2,...
FROM table_name
LIMIT number_of_rows;
```
```
SELECT first_name, last_name
FROM employees
LIMIT 10;
```
```
Open
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
dvdrental
Query Tool
Schema
public
Tables 
payment
```

## Query 
```
SELECT * FROM payment;
```
```
Data Output
payment_id   customer_id   staff_id   …
…                  …                    …           …
```

## Query 
```
SELECT * FROM payment ORDER BY payment_date ASC;
```
```
Data Output
payment_id   customer_id   staff_id   …
…                  …                    …           …
```

## Query 
```
SELECT * FROM payment ORDER BY payment_date DESC;
```
```
Data Output
payment_id   customer_id   staff_id   …
…                  …                    …           …
```

BETWEEN 

```
SELECT column_name(s)
FROM table_name
WHERE column_name BETWEEN
value1 AND value2;
```

```
SELECT order_id, order_date
FROM orders
WHERE order_date BETWEEN ‘2023-01-01’ AND ‘2023-06-30’;
```

```
SELECT employee_id, first_name, last_name, salary
FROM employees
WHERE salary BETWEEN 40000 AND 60000;
```

```
Open
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
dvdrental
Query Tool
Schema
public
Tables 
payment
```

## Query 
```
SELECT * FROM payment
LIMIT 5;
```
```
Data Output
payment_id   customer_id   staff_id   …
…                  …                    …           …
```

## Query 
```
SELECT * FROM payment
WHERE amount BETWEEN 8 AND 9
LIMIT 5;
```
```
Data Output
payment_id   customer_id   staff_id   …
…                  …                    …           …
```

## Query 
```
SELECT * FROM payment
WHERE amount NOT BETWEEN 8 AND 9
LIMIT 5;
```
```
Data Output
payment_id   customer_id   staff_id   …
…                  …                    …           …
```
## Query 
```
SELECT COUNT(*) FROM payment
WHERE amount NOT BETWEEN 8 AND 9;
```
```
Data Output
count
14157
```
## Query 
```
SELECT * FROM payment
WHERE payment_date BETWEEN ‘2007-02-01’ AND ‘2007-02-15’
```
```
Data Output
payment_id   customer_id   staff_id   …
…                  …                    …           …
```

## Query 
```
SELECT * FROM payment ORDER BY payment_date ASC
LIMIT 10;
```
```
Data Output
payment_id   customer_id   staff_id   …
…                  …                    …           …
```

## Query 
```
SELECT * FROM payment 
WHERE amount != 0.99
ORDER BY payment_date
LIMIT 10;
```
```
Data Output
payment_id   customer_id   staff_id   …
…                  …                    …           …
```

IN

```
SELECT column_name(s)
FROM table_name
WHERE column_name IN (value1, value2,...);
```

```
Open
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
dvdrental
Query Tool
Schema
public
Tables 
payment
```

## Query
```
SELECT * FROM payment
LIMIT 5;
```
```
Data Output
payment_id   customer_id   staff_id   …
…                  …                    …           …
```

## Query
```
SELECT DISTINCT (amount) FROM payment;
```
```
Data Output
amount
1.99
…
```

## Query
```
SELECT * FROM payment
WHERE amount IN (‘0.99’,‘1.98’,‘1.99’);
```
```
Data Output
payment_id   customer_id   staff_id   …
…                  …                    …           …
```

## Query
```
SELECT * FROM payment
WHERE amount NOT IN (‘0.99’,‘1.98’,‘1.99’);
```
```
Data Output
payment_id   customer_id   staff_id   …
…                  …                    …           …
```

## Query
```
SELECT * FROM customer
WHERE first_name IN (‘John’,‘jake’,‘Julie’);
```
```
Data Output
payment_id   customer_id   staff_id   …
…                  …                    …           …
```

LIKE or ILIKE

```
SELECT column_name(s)
FROM table_name
WHERE column_name LIKE pattern;
```

```
SELECT column_name(s)
FROM table_name
WHERE column_name ILIKE pattern;
```

```
SELECT customer_name, contact_email
FROM customers
WHERE customer_name LIKE ‘J%’;
```

```
SELECT product_name, category
FROM products
WHERE product_name LIKE ‘%blue%’;
```

```
SELECT first_name, last_name
FROM employees
WHERE last_name ILIKE ‘%son’;
```

```
SELECT product_name
FROM products
WHERE product_name LIKE ‘%apple%’;
```

```
SELECT customer_name
FROM customers
WHERE customer_name LIKE ‘J_n%’;
```

```
SELECT product_name
FROM products
WHERE product_name LIKE ‘colo[u]r%’;
```

```
SELECT email_address
FROM users
WHERE email_address LIKE ‘%example[_].[cno]m’;
```

```
Open
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
dvdrental
Query Tool
Schema
public
Tables 
customer 
```

## Query 
```
SELECT * FROM customer;
```
```
Data Output 
customer_id   store_id   first_name   …
…                   …            …                …
```

## Query 
```
SELECT * FROM customer WHERE first_name LIKE ‘J%’;
```
```
Data Output 
customer_id   store_id   first_name   …
…                   …            …                …
```

## Query 
```
SELECT COUNT(*) FROM customer WHERE first_name LIKE ‘J%’;
```
```
Data Output 
count
65
```

## Query 
```
SELECT * FROM customer WHERE first_name LIKE ‘J%’ AND last_name LIKE ‘S%’;
```
```
Data Output 
customer_id   store_id   first_name   …
…                   …            …                …
```

## Query 
```
SELECT * FROM customer WHERE first_name ILIKE ‘J%’ AND last_name ILIKE ‘S%’;
```
```
Data Output 
customer_id   store_id   first_name   …
…                   …            …                …
```

## Query 
```
SELECT * FROM customer 
WHERE first_name LIKE ‘%er%’;
```
```
Data Output 
customer_id   store_id   first_name   …
…                   …            …                …
```

## Query 
```
SELECT * FROM customer 
WHERE first_name LIKE ‘_er%’;
```
```
Data Output 
customer_id   store_id   first_name   …
…                   …            …                …
```

## Query 
```
SELECT * FROM customer 
WHERE first_name LIKE ‘_er_’;
```
```
Data Output 
customer_id   store_id   first_name   …
…                   …            …                …
```

## Query 
```
SELECT * FROM customer 
WHERE first_name NOT LIKE ‘_er_’;
```
```
Data Output 
customer_id   store_id   first_name   …
…                   …            …                …
```

Basic Retrieval 

```
SELECT first_name, last_name, email
FROM customer;
```

Conditional Retrieval

```
SELECT payment_id, customer_id, amount
FROM payment WHERE amount > 100;
``` 

Sorting and Limiting

```
SELECT first_name, last_name, email
FROM customer ORDER BY last_name ASC LIMIT 5;
```

Data Filtering 

```
SELECT payment_id, customer_id, payment_date
FROM payment WHERE EXTRACT (year FROM payment_date) = 2022;
```

Pattern Matching 

```
SELECT first_name, last_name, email 
FROM customer WHERE email LIKE ‘%gmail%’;
```

Range Query

```
SELECT payment_id, customer_id, amount
FROM payment WHERE amount BETWEEN 50 AND 100;
```

AGGREGATE 

```
Open
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
dvdrental
Query Tool
Schema
public
Tables 
film
```

## Query 
```
SELECT * FROM film;
```
```
Data Output
film_id   title   description   …
…          …     …                …
```

## Query 
```
SELECT MIN(replacement_cost) FROM film;
```
```
Data Output
min
9.99
```

## Query 
```
SELECT MAX(replacement_cost) FROM film;
```
```
Data Output
max
29.99
```

## Query 
``` 
SELECT MAX(replacement_cost), MIN(replacement_cost) FROM film;
```
```
Data Output
max      min
29.99    9.99
```

## Query 
```
SELECT AVG(replacement_cost) FROM film;
```
Data Output
avg
19.98400
```

## Query 
```
SELECT ROUND(AVG(replacement_cost), 3) FROM film;
```
```
Data Output
avg
19.984
```

## Query 
```
SELECT SUM(replacement_cost) FROM film;
```
```
Data Output
sum
19984.00
```

GROUP BY

```
Open
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
dvdrental
Query Tool
Schema
public
Tables 
payment
```

## Query
```
SELECT * FROM payment;
Data Output
payment_id   customer_id   staff_id    …
…                  …                   …            …
```

## Query
```
SELECT customer_id FROM payment
GROUP BY customer_id;
```
```
Data Output
customer_id  
184
…
```

## Query
```
SELECT customer_id, SUM FROM payment
GROUP BY customer_id;
```
```
Data Output
customer_id  sum
184                80.80 
…                  …
```

## Query
```
SELECT customer_id, SUM FROM payment
GROUP BY customer_id
ORDER BY SUM (amount);
```
```
Data Output
customer_id  sum
318                27.93 
…                  …
```

## Query
```
SELECT customer_id, SUM FROM payment
GROUP BY customer_id
ORDER BY SUM (amount) ASC;
```
```
Data Output
customer_id  sum
318                27.93 
…                  …
```

## Query
```
SELECT customer_id, SUM FROM payment
GROUP BY customer_id
ORDER BY SUM (amount) DESC;
```
```
Data Output
customer_id  sum
148                211.55 
…                  …
```

## Query
```
SELECT * FROM payment
```
```
Data Output
payment_id   customer_id   staff_id    …
…                  …                   …            …
```

## Query
```
SELECT customer_id, staff_id, SUM(amount) FROM payment
GROUP BY customer_id, staff_id 
ORDER BY SUM(amount);
```
```
Data Output
customer_id   staff_id    sum   …
…                   …             …      …
```

## Query
```
SELECT * FROM payment
```
```
Data Output
payment_id   customer_id   staff_id    …
…                  …                   …            …
```

## Query
```
SELECT DATE(payment_date), SUM(amount) FROM payment
GROUP BY DATE(payment_date)
ORDER BY SUM(amount);
```
```
Data Output
date                  sum
2007-02-14      116.73
…                      …
```

## Query
```
SELECT customer_id, COUNT(amount) FROM payment
GROUP BY customer_id
ORDER BY COUNT(amount);
```
```
Data Output
customer_id    count
318                 7
…                    …
```

```
SELECT staff_id, SUM(amount) FROM payment 
GROUP BY staff_id;
```

```
SELECT payment_id, amount, payment_date
FROM payment 
WHERE payment_date = ‘YYYY-MM-DD’;
```

HAVING

```
SELECT column1, aggregate_function(column2)
FROM table
GROUP BY column1
HAVING condition;
```

```
SELECT department, COUNT(*) FROM employees
GROUP BY department
HAVING COUNT(*) > 10;
```

```
SELECT department, AVG(salary) FROM employees
GROUP BY department 
HAVING AVG(salary) > 50000;
```

```
Open
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
dvdrental
Query Tool
Schema
public
Tables 
payment
```

## Query 
```
SELECT * FROM payment;
```
```
Data Output 
payment_id   customer_id   staff_id   …
…                  …                   …           …
``` 

## Query 
```
SELECT customer_id, SUM(amount) FROM payment
GROUP BY customer_id
```
```
Data Output 
customer_id   sum 
1.84                80.80               
```

## Query 
```
SELECT customer_id, SUM(amount) FROM payment
WHERE customer_id NOT IN (184, 87)
GROUP BY customer_id;
```
```
Data Output 
customer_id   sum 
1.84                80.80     
```

## Query 
```
SELECT customer_id, SUM(amount) FROM payment
GROUP BY customer_id;
HAVING SUM(amount) > 100
```
```
Data Output 
customer_id   sum 
…                   …
```

## Query 
```
SELECT * FROM customer;
```
```
Data Output 
customer_id   store_id   first_name   …
…                   …            …                 …
```

## Query 
```
SELECT store_id, COUNT(customer_id)  FROM customer;
GROUP BY store_id 
```
```
Data Output 
store_id   count   
1              326
```

## Query 
```
SELECT store_id, COUNT(customer_id)  FROM customer;
GROUP BY store_id 
HAVING COUNT(customer_id) > 300
```
```
Data Output 
store_id   count   
1              326
```

## Query 
```
SELECT store_id, COUNT(*)  FROM customer;
GROUP BY store_id 
HAVING COUNT(*) > 300
```
```
Data Output 
store_id   count   
1              326
```

AS 

```
SELECT original_name AS new_name
FROM table_name;
```

```
Open
pgAdmin 4
Object Explorer
Servers
PostgreSQL 15
dvdrental
Query Tool
Schema
public
Tables 
payment
```

## Query 
```
SELECT * FROM payment;
```
```
Data Output
payment_id customer_id staff_id …
…                …                  …        …
```

## Query 
```
SELECT COUNT(amount) FROM payment;
```
```
Data Output
count
14596
```

## Query 
```
SELECT COUNT(amount) AS number_transactions FROM payment;
```
```
Data Output
count
14596
```

## Query 
```
SELECT customer_id, SUM(amount) FROM payment
GROUP BY customer_id;
```
```
Data Output
customer_id   sum 
…                 …
```
## Query 
```
SELECT customer_id, SUM(amount) AS total_spent FROM payment
GROUP BY customer_id
HAVING SUM(amount) > 100;
```
```
Data Output
customer_id   total_spent
…                   …
```



