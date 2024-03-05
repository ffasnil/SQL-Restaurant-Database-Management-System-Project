# A Restaurant Database Management System Project using SQL

This project consists of 3 main parts:
1. Creating Tables
2. Inserting Items Into Tables
3. Querying Information from Multiple Tables

To explore the project, you can visit it on Replit: [https://replit.com/@supisaranilkasa/RestaurantSQLDB?v=1#main.sql](https://replit.com/@supisaranilkasa/RestaurantSQLDB?v=1#main.sql)

<br>

### <ins>ER Diagram</ins>
The diagram was created via: [https://www.quickdatabasediagrams.com/](https://www.quickdatabasediagrams.com/)

![QuickDBD-export](https://github.com/ffasnil/SQL-Restaurant-Database-Management-System-Project/assets/89661712/57a1f8c2-26cb-44a9-873a-46d4e917fb2e)

### <ins>Output</ins>
After running the code in the final section, which executed the query to retrieve necessary information from multiple connected tables, the resulting output is displayed below. Additionally, there has been a calculation for the TotalPrice.

```
SELECT
    co.OrderID,
    co.OrderDate,
    c.FirstName || ' ' || c.LastName AS CustomerFullName,
    m.MenuName,
    co.Quantity,
    m.Price,
    m.Price * co.Quantity AS TotalPrice,
    b.City AS BranchCity
FROM CustomerOrder co
JOIN Customer c ON co.CustomerID = c.CustomerID
JOIN Employee e ON co.EmployeeID = e.EmployeeID
JOIN Menu m ON co.MenuID = m.MenuID
JOIN Branch b ON e.BranchID = b.BranchID;
```
![Screenshot (57)](https://github.com/ffasnil/SQL-Restaurant-Database-Management-System-Project/assets/89661712/51f43a3c-b266-4b04-9310-23366acd76a9)
