# SQL- Cases
SQL QUESTIONS THAT I HAVE SOLVED FROM LEADCODE AND VARIOUS WEBSITE.

### CASE - Order Fulfillment
You are given two tables: products and orders. The products table contains information about each product, including the product ID and available quantity in the warehouse. The orders table contains details about customer orders, including the order ID, product ID, order date, and quantity requested by the customer.
Write an SQL query to generate a report listing the orders that can be fulfilled based on the available inventory in the warehouse, following a first-come-first-serve approach based on the order date. Each row in the report should include the order ID, product name, quantity requested by the customer, quantity actually fulfilled, and a comments column as below:
If the order can be completely fulfilled then 'Full Order',If the order can be partially fullfilled then 'Partial Order',If order can not be fulfilled at all then 'No Order'.
## DATA 
![OF TABLE](https://github.com/user-attachments/assets/7d21d7e2-7209-4862-8a5c-de322f6b269d)

## SOLUTION 
![OF QUERY](https://github.com/user-attachments/assets/9f6baf28-52fa-4290-aa03-1510144b8384)

## OUTPUT
![OF SOL](https://github.com/user-attachments/assets/e147b250-5274-45ea-8107-e577fbbe4a2f)


### CASE - DYNAMIC PRICING
You are given a products table where a new row is inserted every time the price of a product changes. Additionally, there is a transaction table containing details such as order_date and product_ID for each order. Write an SQL query to calculate the total sales value for each product, considering the cost of the product at the time of the order date.
## DATA
![19d](https://github.com/user-attachments/assets/7d83b2c2-3636-4ee6-8d10-20e6360df7c4)

## SOLUTION
![19S](https://github.com/user-attachments/assets/2a90e1a7-5f6b-42b4-9fc4-6613302921a9)


### CASE - Highly Paid Employees
You are given the data of employees along with their salary and department . Write an SQL to find list of employees who has salary greater than average employee salary of the company.  However , While calculating the company average salary to compare with an employee salary do not consider salaries of that employee's department.

## DATA 
![HIGEST PAID EMP Q](https://github.com/user-attachments/assets/c3b1f309-6b1b-446a-8191-d7024489b025)

## SOLUTION 
![HIGEST PAID EMP SOL](https://github.com/user-attachments/assets/a3e40ba9-9f9b-4960-babc-bd01d9144bfe)


### CASE - New and Repeat Customers
NamasteKart an ecommerce company wants to build a very imporant business metrics where they want to track on daily basis how many new and repeat customers are purchasing products from their website. A new customer is defined when he purchased anything for the first time from the website and repeat customer is someone who has done atleast one purchase in the past.
## DATA 
![11 Q](https://github.com/user-attachments/assets/55f5ef21-fdad-4968-baa4-45a7edd0753b)

## SOLUTION
![11 Q](https://github.com/user-attachments/assets/55f5ef21-fdad-4968-baa4-45a7edd0753b)





