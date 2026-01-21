Bank Management System (Java | JDBC | MySQL)

1.Project Overview

The Bank Management System is a Java-based console application designed to manage bank account records efficiently. The project demonstrates CRUD operations (Create, Read, Update, Delete) using JDBC to interact with a MySQL database, following a Layered Architecture approach.


2.Technologies Used

| Technology  | Description                |
| ----------- | -------------------------- |
| Java        | Core programming language  |
| JDBC        | Java Database Connectivity |
| MySQL       | Relational Database        |
| Eclipse IDE | Development Environment    |



3.Project Structure (Layered Architecture)

BankManagementSystem
│
├── com.bank.model          → Model / POJO classes
├── com.bank.dao            → DAO interfaces
├── com.bank.dao.impl       → DAO implementations
├── com.bank.service        → Service interfaces
├── com.bank.service.impl   → Service implementations
├── com.bank.util           → Database utility
└── com.bank.main           → Main (UI) class


 
4.Database Details

Database Name -bankdb
sql
CREATE DATABASE bankdb;
USE bankdb;

CREATE TABLE account (
    acc_no INT PRIMARY KEY,
    name VARCHAR(50),
    balance DOUBLE
);

5.Package & Class Description

-Model Layer (`com.bank.model`)
 Account.java
 Represents bank account entity
 Contains account number, name, and balance
 Uses encapsulation (private variables with getters and setters)

-Utility Layer (`com.bank.util`)
 DBUtil.java
 Establishes database connection
 Loads MySQL JDBC driver
 Returns reusable `Connection` object

-DAO Layer (`com.bank.dao`, `com.bank.dao.impl`)
 AccountDao.java
 DAO interface
 Declares CRUD methods

-AccountDaoImpl.java

 Implements DAO interface
 Contains SQL queries
 Uses `PreparedStatement` to prevent SQL injection

- Service Layer (`com.bank.service`, `com.bank.service.impl`)
 AccountService.java
 Defines business operations

-AccountServiceImpl.java
   Implements service interface
   Acts as bridge between Main and DAO layer

- Main Layer (`com.bank.main`)
  BankMain.java
  Entry point of application
  Menu-driven console UI
  Accepts user input using `Scanner`

6.Sample Menu Output

1. Add Account
2. Update Account
3. Delete Account
4. View Account
5. View All Accounts
6. Exit


7.OOP Concepts Used

* Encapsulation
* Abstraction
* Interface-based programming
* Loose Coupling
* Layered Architecture

8.Advantages

* Clean and organized code
* Easy to modify and extend
* Real-world application design
* Ideal for learning JDBC and architecture

9.Future Enhancements

* GUI using Swing or JavaFX
* Deposit & Withdraw functionality
* Transaction history
* User authentication
* Hibernate / Spring Boot integration

10.Conclusion

The Bank Management System project demonstrates a complete Java application using JDBC, MySQL, and Layered Architecture. It is well-structured, easy to understand, and suitable for academic as well as learning purposes.
