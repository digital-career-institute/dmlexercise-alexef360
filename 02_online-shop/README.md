# Online Shop 

## Create a new database
Create a new database for this exercise.
```
CREATE DATABASE exercise_online_shop
use exercise_online_shop
``

## Create the product table
Create a table named **products** with the following columns:  
```
product_id (integer, primary key)
product_name (varchar, maximum length 100)
price (decimal, 2 decimal places)
stock_quantity (integer)
```

> ANSWER
CREATE TABLE products (
    product_id INT PRIMARY KEY,
    product_name VARCHAR(100),
    price DECIMAL(10 , 2 ),
    stock_quantity INT
);

## Insert and select Data
### 1. Insert Data
Insert these records into the products table with the following data:
```
(1, 'Laptop', 999.99, 20)
(2, 'Smartphone', 499.50, 30)
(3, 'Headphones', 79.99, 50)
(4, 'Tablet', 299.75, 15)
(5, 'Bluetooth Speaker', 39.95, 40)
(6, 'Keyboard', 29.95, 10)
```

> ANSWER
insert into products values (1, 'Laptop', 999.99, 20),
 (2, 'Smartphone', 499.50, 30),
 (3, 'Headphones', 79.99, 50),
 (4, 'Tablet', 299.75, 15),
 (5, 'Bluetooth Speaker', 39.95, 40),
 (6, 'Keyboard', 29.95, 10);

### Select Products 
Write a query to retrieve the **names and prices** of all products.

> ANSWER
SELECT 
    product_name, price
FROM
    products;

### Search expensive products
Write a query to select products with a price greater than $100.

> ANSWER
SELECT 
    product_name, price
FROM
    products
WHERE
    price > 100;

### Search low stock
Write a query to retrieve the **names an prices** of all products with a stock less than 30.

> ANSWER
SELECT 
    product_name, stock_quantity
FROM
    products
WHERE
    stock_quantity < 30;

### Bonus: Select expensive out of stock products
Write a query to retrieve the **names and prices** of all products with a price greater than $100 and a stock less than 30.

> ANSWER  
SELECT 
    product_name, price
FROM
    products
WHERE
    price > 100 AND stock_quantity < 30;
