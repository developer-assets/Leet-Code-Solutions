# 584. Find Customer Referee

## Problem Desription

This SQL query retrieves the names of customers who were not referred by the customer with id = 2. It selects the names from the Customer table where the referee_id is not equal to 2 or is NULL (indicating that the customer was not referred by anyone).

## Question

 - Find the names of the customer that are not referred by the customer with `id = 2`.
 - Return the result table in any order.

## SQL Schema

```sql
  CREATE TABLE Customer (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    referee_id INT
  );
```

## Example

Consider the following `Customer` table:

| id         | name     | referee_id |
|------------|----------|------------|
| 1          | Will     | Null       |
| 2          | Jane     | Null       |
| 3          | Alex     | 2          |
| 4          | Bill     | Null       |
| 5          | Zack     | 1          |
| 6          | Mark     | 2          |

The expected output is:

| name        |
|-------------|
| Will        |
| Jane        |
| Bill        |
| Zack        |

