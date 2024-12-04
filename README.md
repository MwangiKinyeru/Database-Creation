# Database-Creation

## Creating a realistic bank Database

### Nitram Cooperative Bank Database

This project involves designing a realistic banking database for Nitram Cooperative Bank. 
The database structure and datasets were created to simulate real-world operations such as 
customer management, account handling, loans, and transactions.

### Dataset Creation

The data was generated using the Python library Faker, which creates realistic mock data. 
The datasets generated include the following:

Customers: Contains customer details such as name, email, phone, and address.

Branches: Lists branch information like branch name, address, and contact number.

Accounts: Holds details about customer accounts, account types, balances, and opening dates.

Loans: Includes information on customer loans, such as loan amounts, interest rates, and loan duration.

Transactions: Tracks transactions performed on accounts, including deposits, withdrawals, and transfers.

Each dataset was exported as a CSV file for subsequent loading into the PostgreSQL database.

### Database Design

The database was designed using the following schema:

Tables
Customers:

Customer_id (Primary Key)
First_name
Last_name
Email
Phone
Address
Date_of_birth
Branches:

Branch_id (Primary Key)
Branch_name
Branch_address
Branch_phone
Account:

Account_id (Primary Key)
Customer_id (Foreign Key referencing Customers.Customer_id)
Account_type
Balance
Opened_date
Loans:

Loan_id (Primary Key)
Customer_id (Foreign Key referencing Customers.Customer_id)
Loan_amount
Interest_rate
Loan_start_date
Loan_end_date
Transactions:

Transaction_id (Primary Key)
Account_id (Foreign Key referencing Account.Account_id)
Transaction_type
Amount
Transaction_date
Description
Relationships
The Customers table is linked to Account and Loans through foreign keys.
The Account table is linked to Transactions.

### Database Creation
PostgreSQL Setup:

A database named Nitram Cooperative Bank was created in PostgreSQL.
The tables were created using SQL scripts with appropriate constraints (e.g., primary and foreign keys).
Table Creation: SQL commands were used to create tables as defined in the schema above. 



