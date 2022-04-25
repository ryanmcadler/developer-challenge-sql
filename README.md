# developer-challenge-sql

## Installation
Clone the repo.  If you will be executing any queries, you will need to install sqlite3.  In this exercise, you are encouraged to write sql files containing various queries intended to solve the problem at hand.  To execute a sql file against a sqlite3 database, you can use a pattern similar to the following:L

```
sqlite3 db/customer_admin.db < sql_query.sql
```

## The Exercise
There is a sqlite3 database located at `/db/customer_admin.db` that contains a simple database for an ordering system; there a three tables with the following attributes:

- Products
    - ID (integer, primary key)
    - Name (text)
    - Product Type (text)
    - Cost (numeric)
- Orders
    - ID (integer, primary key)
    - Product ID (integer, foreign key)
    - Customer ID (ineger, foreign key)
    - Amount (numeric)
    - Order Date (string)
- Customers
    - Name (text)
    - Contact First Name (text)
    - Contact Last Name (text)
    - Contact Email (text)
    - Contact Phone (text) 
    - Country (text)

We need to answer the following questions by writing a single SQL query:

1. What were the last 5 orders, and what was the associated product name and customer name?
2. What is the average amount spent in an order?
3. What is the most popular product?
4. There are two customers that we want to compare orders for (Custom A and Customer B).  What products were purchased by both customers?
5. There is a record in the orders database that does not have a valid product (the product record was somehow deleted at one point).  How do we write a query to identify this record?