# DB Connection - Java Web Application

## 📌 Project Description

DB Connection is a simple Java web application developed using JSP, Servlets, JDBC, and MySQL.

The project demonstrates how to connect a Java web application to a MySQL database and perform basic user registration and login operations.

## ✨ Features

- User Registration
- User Login
- MySQL Database Connection
- JDBC Connectivity
- Session Management
- Login Validation
- PreparedStatement for database queries
- JSP-based web pages
- Servlet-based backend processing

## 🛠 Technologies Used

- Java
- JSP (JavaServer Pages)
- Jakarta Servlets
- JDBC
- MySQL
- Apache Tomcat
- Eclipse IDE
- HTML
- CSS

## 📂 Project Structure

```text
DB_Connection
│
├── src/main/java
│   └── com/corejava
│       ├── DBConnection.java
│       ├── LoginServlet.java
│       ├── RegisterServlet.java
│       └── TestConnection.java
│
├── src/main/webapp
│   ├── index.jsp
│   ├── register.jsp
│   ├── login.jsp
│   ├── home.jsp
│   │
│   └── WEB-INF
│       ├── web.xml
│       └── lib
│           └── mysql-connector-java-5.1.23.jar
│
├── .classpath
└── .project
```

## 📄 Main Java Files

### DBConnection.java

This class is responsible for establishing the connection between the Java application and the MySQL database using JDBC.

### RegisterServlet.java

This servlet receives user registration details such as:

- Name
- Email
- Username
- Password

It stores the user information in the MySQL database.

### LoginServlet.java

This servlet validates the username and password entered by the user.

If the credentials are correct, the user is redirected to the home page.

### TestConnection.java

This class is used to test whether the Java application is successfully connected to the MySQL database.

## 🗄️ Database Configuration

The project uses the following database:

```text
Database Name: corejava_training
```

Create the database in MySQL:

```sql
CREATE DATABASE corejava_training;

USE corejava_training;
```

Create the `users` table:

```sql
CREATE TABLE users (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    email VARCHAR(100),
    username VARCHAR(100),
    password VARCHAR(100)
);
```

## ⚙️ Database Connection

Update the database credentials in `DBConnection.java` according to your MySQL configuration.

Example:

```java
private static final String URL =
        "jdbc:mysql://localhost:3306/corejava_training";

private static final String USER = "root";

private static final String PASSWORD = "your_mysql_password";
```

> Do not upload your real database password or other sensitive credentials to a public GitHub repository.

## ▶️ How to Run the Project

1. Open Eclipse IDE.
2. Import the `DB_Connection` project.
3. Configure Apache Tomcat Server in Eclipse.
4. Make sure MySQL Server is running.
5. Create the `corejava_training` database.
6. Create the `users` table.
7. Update the MySQL username and password in `DBConnection.java`.
8. Add the project to the Tomcat server.
9. Right-click the project.
10. Select **Run As → Run on Server**.
11. Select the configured Tomcat server.
12. Open the application in the browser.

## 🔄 Application Flow

```text
User
  ↓
Registration Page
  ↓
RegisterServlet
  ↓
MySQL Database
  ↓
Login Page
  ↓
LoginServlet
  ↓
User Authentication
  ↓
Home Page
```

## 🔐 Login Process

The application checks the entered username and password against the data stored in the `users` table.

If the credentials are valid:

```text
Login Successful → Home Page
```

If the credentials are invalid:

```text
Login Failed → Try Again
```

## 📚 Concepts Demonstrated

- Java Database Connectivity (JDBC)
- MySQL Database Connection
- JSP
- Jakarta Servlets
- HTTP POST Requests
- PreparedStatement
- ResultSet
- Session Management
- Exception Handling
- User Registration and Authentication


## 📌 Purpose

This project was developed to understand how Java web applications connect with MySQL databases and how JSP, Servlets, JDBC, and Tomcat work together to implement registration and login functionality.
