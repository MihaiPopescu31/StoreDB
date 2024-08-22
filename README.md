# StoreDB

This repository contains the SQL dump for the `storedb` database, which includes schema definitions and sample data.

![image](https://github.com/user-attachments/assets/9374ec4f-3703-4efc-8902-b0cddc62724f)


## Repository Contents

- **storedb.sql**: SQL dump file containing the `storedb` database schema and data.

## Setup Instructions

### 1. **Download the SQL File**

1. Go to the [StoreDB GitHub repository](https://github.com/MihaiPopescu31/StoreDB).
2. Download the `storedb.sql` file from the repository.

### 2. **Create a Database**

**Open MySQL Command Line or phpMyAdmin**

   You can use MySQL command line or a tool like phpMyAdmin to create the database.

**Using phpMyAdmin**

- Open phpMyAdmin.
- Select the newly created storedb database.
- Go to the Import tab.
- Choose the storedb.sql file.
- Click Go to start the import process.


### 3. **Database Overview: storedb**

- The storedb database is designed for managing customer orders. It includes five key tables:

 #### customer: Stores customer details.

 - Fields: CustomerID (PK), CustomerName, CustomerSurName, CustomerAge.
 #### address: Stores customer addresses.

 - Fields: AddressID (PK), CustomerID (FK), AddressDetails, CityAddress.
####  order: Stores orders placed by customers.

 - Fields: OrderID (PK), CustomerID (FK), AddressID (FK).
#### order_item: Details items within each order.

- Fields: OrderItemID (PK), OrderID (FK), ProductID (FK), OrderItemQty.
#### product: Stores product details.

 - Fields: ProductID (PK), ProductName, ProductPrice.



### Relationships
 - Customer to Address: One-to-many (one customer can have multiple addresses).
 - Customer to Order: One-to-many (one customer can place multiple orders).
 - Order to OrderItem: One-to-many (one order can have multiple items).
 - OrderItem to Product: Many-to-one (many order items can refer to one product).


### 4. **Usage**
You can use the storedb database for development and testing. The provided schema and sample data will help in setting up a working environment.
