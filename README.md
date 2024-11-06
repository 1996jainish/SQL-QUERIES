# SQL- Cases
SQL QUESTIONS THAT I HAVE SOLVED FROM LEADCODE AND VARIOUS WEBSITE.

### CASE 01 - Order Fulfillment
You are given two tables: products and orders. 
The products table contains information about each product, including the product ID and available quantity in the warehouse. The orders table contains details about customer orders, including the order ID, product ID, order date, and quantity requested by the customer.
Write an SQL query to generate a report listing the orders that can be fulfilled based on the available inventory in the warehouse, following a first-come-first-serve approach based on the order date. Each row in the report should include the order ID, product name, quantity requested by the customer, quantity actually fulfilled, and a comments column as below:
If the order can be completely fulfilled then 'Full Order',If the order can be partially fullfilled then 'Partial Order',If order can not be fulfilled at all then 'No Order'.
DATA 
![OF TABLE](https://github.com/user-attachments/assets/7d21d7e2-7209-4862-8a5c-de322f6b269d)

SOLUTION 
![OF QUERY](https://github.com/user-attachments/assets/9f6baf28-52fa-4290-aa03-1510144b8384)

OUTPUT
![OF SOL](https://github.com/user-attachments/assets/e147b250-5274-45ea-8107-e577fbbe4a2f)


### CASE 02 - DYNAMIC PRICING
You are given a products table where a new row is inserted every time the price of a product changes. Additionally, there is a transaction table containing details such as order_date and product_ID for each order. Write an SQL query to calculate the total sales value for each product, considering the cost of the product at the time of the order date.
DATA
![19d](https://github.com/user-attachments/assets/7d83b2c2-3636-4ee6-8d10-20e6360df7c4)

SOLUTION
![19S](https://github.com/user-attachments/assets/2a90e1a7-5f6b-42b4-9fc4-6613302921a9)


### CASE 03 - Highly Paid Employees
You are given the data of employees along with their salary and department . Write an SQL to find list of employees who has salary greater than average employee salary of the company.  However , While calculating the company average salary to compare with an employee salary do not consider salaries of that employee's department.

DATA 
![HIGEST PAID EMP Q](https://github.com/user-attachments/assets/c3b1f309-6b1b-446a-8191-d7024489b025)

SOLUTION 
![HIGEST PAID EMP SOL](https://github.com/user-attachments/assets/a3e40ba9-9f9b-4960-babc-bd01d9144bfe)


### CASE 04 - Zomato Customer Behaviour 
![Screenshot 2024-08-20 180547](https://github.com/user-attachments/assets/f2ba1402-b551-43ef-9fa9-33335b194a8a)

solution - 
![Screenshot (70)](https://github.com/user-attachments/assets/686a7a3d-6c6b-4e8e-8e8f-4ae39fefa1e8)

output - 
![Screenshot 2024-08-20 180619](https://github.com/user-attachments/assets/0a039cfe-e4b9-4c06-924c-0695915834dd)


### CASE 05 - Cricket Score Table
![Screenshot 2024-08-20 202714](https://github.com/user-attachments/assets/67123f24-6dac-4b82-a7b8-c65fc198df1e)

Solution - 
![Screenshot (71)](https://github.com/user-attachments/assets/cd6b9117-650f-41ef-a7e0-c82575a23484)

Output - 
![Screenshot 2024-08-20 202747](https://github.com/user-attachments/assets/f0280b98-1995-49bb-afca-eb918f626f09)


### SQL Questions with Easy - Medium level difficulty
### Question 1 
Namastekart, an e-commerce company, has observed a notable surge in return orders recently. 
They suspect that a specific group of customers may be responsible for a significant portion of these returns. 
To address this issue, their initial goal is to identify customers who have returned more than 50% of their orders. 
This way, they can proactively reach out to these customers to gather feedback.

Write an SQL to find list of customers along with their return percent (Round to 2 decimal places), display the output in ascending order of customer name.

Table: orders (primary key : order_id)
+---------------+-------------+
| COLUMN_NAME   | DATA_TYPE   |
+---------------+-------------+
| customer_name | varchar(10) |
| order_date    | date        |
| order_id      | int         |
| sales         | int         |
+---------------+-------------+

Table: returns (primary key : order_id)
+-------------+-----------+
| COLUMN_NAME | DATA_TYPE |
+-------------+-----------+
| order_id    | int       |
| return_date | date      |
+-------------+-----------+

Solution - 
SELECT O.customer_name, 
Round(SUM(CASE WHEN R.return_date IS NULL THEN 0 ELSE 1 END)/COUNT(O.customer_name)*100,2) as return_percen
FROM orders O
LEFT JOIN returns R ON R.order_id = O.order_id
GROUP BY O.customer_name
HAVING return_percent >= 50




