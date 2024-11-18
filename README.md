# northwind-database
Q1 Show the category_name and description from the categories table sorted by category_name.
`SELECT category_name, description
FROM categories
ORDER BY category_name;`

Q2 Show all the contact_name, address, city of all customers which are not from 'Germany', 'Mexico', 'Spain'

`SELECT contact_name, address, city 
FROM customers
where country NOT IN ('Germany', 'Mexico', 'Spain');
`

Q3 Show order_date, shipped_date, customer_id, Freight of all orders placed on 2018 Feb 26

`SELECT order_date, shipped_date, customer_id, freight 
FROM orders
where order_date = '2018-02-26';`

Q4 Show the employee_id, order_id, customer_id, required_date, shipped_date from all orders shipped later than the required date

`SELECT employee_id, order_id, customer_id, required_date, shipped_date
FROM orders
WHERE shipped_date > required_date;`


Q5 Show all the even numbered Order_id from the orders table

`SELECT order_id
FROM orders
WHERE order_id % 2 = 0;`

Q6 Show the city, company_name, contact_name of all customers from cities which contains the letter 'L' in the city name, sorted by contact_name

`SELECT city, company_name, contact_name
FROM customers
WHERE city LIKE '%L%'
ORDER BY contact_name`

Q7 Show the company_name, contact_name, fax number of all customers that has a fax number. (not null)

`SELECT  company_name, contact_name, fax
FROM customers
where fax is not null;`

Q8 Show the first_name, last_name. hire_date of the most recently hired employee.

`SELECT  first_name, last_name, max(hire_date) as hire_date
FROM employees`

Q9 Show the average unit price rounded to 2 decimal places, the total units in stock, total discontinued products from the products table.

`SELECT round(avg(Unit_Price), 2) AS average_price,
SUM(units_in_stock) AS total_stock,
SUM(discontinued) as total_discontinued
FROM products;`

Q10 Show the ProductName, CompanyName, CategoryName from the products, suppliers, and categories table [Medium]

`SELECT p.product_name, s.company_name, c.category_name
FROM products p
JOIN suppliers s ON s.supplier_id = p.Supplier_id
JOIN categories c On c.category_id = p.Category_id;`

Q11 Show the category_name and the average product unit price for each category rounded to 2 decimal places.

`SELECT c.category_name, round(avg(p.unit_price),2) as average_unit_price
FROM products p
JOIN categories c On c.category_id = p.Category_id
GROUP BY c.category_name` 

Q12 Show the city, company_name, contact_name from the customers and suppliers table merged together.
Create a column which contains 'customers' or 'suppliers' depending on the table it came from.

` 
Q13

Q14

Q15

Q16


