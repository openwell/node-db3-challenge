# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 76 records.
    SELECT "CategoryName","ProductName" FROM products;
### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.
    SELECT "OrderID", "ShipperName" FROM Orders JOIN Shippers ON Orders.ShipperID=Shippers.ShipperID WHERE OrderDate < "1997-01-09"
### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.
    SELECT p.ProductName, o.Quantity FROM OrderDetails o left join Products p on p.ProductID = o.ProductID where o.OrderID = "10251"
### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.
    SELECT o.OrderID, c.CustomerName, e.LastName FROM Orders o left join Employees e on e.EmployeeID = o.EmployeeID left join Customers c on c.CustomerID = o.EmployeeID
### (Stretch)  Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a  column called ItemCount that shows the total number of products placed on the order. Shows 196 records. 