# library-management--system
online library-management-system
/* MS SQL Server Script: 
   Database, Table, and Data Creation
*/

-- 1. Create the Database
IF NOT EXISTS (SELECT * FROM sys.databases WHERE name = 'StoreDB')
BEGIN
    CREATE DATABASE StoreDB;
END
GO

-- 2. Switch context to the new database
USE StoreDB;
GO

-- 3. Create the Table
-- 
IF OBJECT_ID('Products', 'U') IS NULL
BEGIN
    CREATE TABLE Products (
        ProductID INT PRIMARY KEY IDENTITY(1,1),
        ProductName NVARCHAR(100) NOT NULL,
        Category NVARCHAR(50),
        Price DECIMAL(10, 2),
        StockQuantity INT,
        DateAdded DATETIME DEFAULT GETDATE()
    );
END
GO

-- 4. Insert Data
INSERT INTO Products (ProductName, Category, Price, StockQuantity)
VALUES 
('Wireless Mouse', 'Electronics', 25.99, 150),
('Mechanical Keyboard', 'Electronics', 89.00, 45),
('Office Chair', 'Furniture', 199.50, 12),
('Desk Lamp', 'Furniture', 34.95, 80);
GO

-- 5. Final Check
SELECT * FROM Products;
GO
/* MS SQL Server Script: 
   Database, Table, and Data Creation
*/

-- 1. Create the Database
IF NOT EXISTS (SELECT * FROM sys.databases WHERE name = 'StoreDB')
BEGIN
    CREATE DATABASE StoreDB;
END
GO

-- 2. Switch context to the new database
USE StoreDB;
GO

-- 3. Create the Table
-- 
IF OBJECT_ID('Products', 'U') IS NULL
BEGIN
    CREATE TABLE Products (
        ProductID INT PRIMARY KEY IDENTITY(1,1),
        ProductName NVARCHAR(100) NOT NULL,
        Category NVARCHAR(50),
        Price DECIMAL(10, 2),
        StockQuantity INT,
        DateAdded DATETIME DEFAULT GETDATE()
    );
END
GO

-- 4. Insert Data
INSERT INTO Products (ProductName, Category, Price, StockQuantity)
VALUES 
('Wireless Mouse', 'Electronics', 25.99, 150),
('Mechanical Keyboard', 'Electronics', 89.00, 45),
('Office Chair', 'Furniture', 199.50, 12),
('Desk Lamp', 'Furniture', 34.95, 80);
GO

-- 5. Final Check
SELECT * FROM Products;
GO

