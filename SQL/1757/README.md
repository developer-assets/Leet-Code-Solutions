# 1757. Recyclable and Low Fat Products

## Problem Description

Given a table of products with columns `product_id`, `low_fats`, and `recyclable`, where `low_fats` and `recyclable` are ENUM types indicating whether the product is low fat ('Y' or 'N') and recyclable ('Y' or 'N') respectively, write an SQL query to find the ids of products that are both low fat and recyclable.

## Question

 - Write a solution to find the ids of products that are both low fat and recyclable.
 - Return the result table in any order.

## SQL Schema

```sql
  CREATE TABLE Products (
    product_id INT PRIMARY KEY,
    low_fats ENUM('Y', 'N'),
    recyclable ENUM('Y', 'N')
  );
```

## Example

Consider the following `Products` table:

| product_id | low_fats | recyclable |
|------------|----------|------------|
| 0          | Y        | N          |
| 1          | Y        | Y          |
| 2          | N        | Y          |
| 3          | Y        | Y          |
| 4          | N        | N          |

The SQL query should return:

| product_id  |
|-------------|
| 1           |
| 3           |
