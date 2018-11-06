1.)
	SELECT * FROM northwind.customers;

2.)
	SELECT DISTINCT Country FROM northwind.customers;

3.)
	SELECT * FROM northwind.customers
	WHERE CustomerID like 'BL%';
	
4.)
	SELECT * FROM northwind.orders
	limit 100;
	
5.)
	SELECT * FROM northwind.customers
	WHERE 
	  (PostalCode = 1010) OR 
	  (PostalCode = 3012) OR 
	  (PostalCode = 12209) OR
	  (PostalCode = 05023);
	  
6.)
	SELECT * FROM northwind.orders
	WHERE ShipRegion like '%';

7.)
	SELECT * FROM northwind.customers
	Order By Country, City;
	
8.)
	INSERT INTO northwind.customers ( CustomerID, CompanyName, ContactName, ContactTitle, Address, City, Region, PostalCode, Country, Phone, Fax, Image, ImageThumbnail )
	Values ('DBACI', 'Dangerous Books and Cakes, Inc', 'Tim Meadows', 'Secretary of Defense', '1601 Pennsylvania Avenue', 'Raccoon City', NULL, '20001', 'Zamunda', '1-555-876-5309', Null, Null, Null );

9.)
	SET SQL_SAFE_UPDATES = 0;
	UPDATE northwind.orders
	SET ShipRegion = 'EuroZone'
	WHERE ShipCountry = 'France';
	
10.)
	DELETE FROM northwind.`order details`
	WHERE Quantity = 1;
	
11.)
	SELECT AVG(Quantity), MAX(Quantity), MIN(Quantity) FROM northwind.`order details`;
	
12.)
	SELECT AVG(Quantity), MAX(Quantity), MIN(Quantity) FROM northwind.`order details`
	GROUP BY orderID;
	
13.)
	SELECT CustomerID FROM northwind.orders
	Where OrderID= 10290;
	
14.)
	SELECT * FROM northwind.customers
	INNER JOIN northwind.orders ON orders.CustomerID = customers.CustomerID
	
	SELECT * FROM Student
	LEFT JOIN Class ON Student.class_id = Class.id

	SELECT * FROM Student
	RIGHT JOIN Class ON Student.class_id = Class.id

15.)
	SELECT FirstName FROM northwind.employees
	Where ReportsTo is NULL;

16.)
	SELECT FirstName FROM northwind.employees
	Where ReportsTo = 2;