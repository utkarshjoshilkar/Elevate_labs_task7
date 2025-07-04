
# Employee Management JDBC App

A simple Java console application to perform CRUD operations on a MySQL database using JDBC.

## Features

* Add, view, update, delete employees
* Batch insert employees
* Logs actions using Java Util Logging

## Tech Stack

* Java (JDK 11)
* MySQL 8.0
* JDBC (mysql-connector-java-8.0.33)
* IntelliJ IDEA

## Project Files

* `Employee.java` – Data model class
* `DatabaseConnection.java` – Handles DB connection
* `EmployeeDAO.java` – Contains CRUD logic
* `Main.java` – Runs test operations

## Setup & Run

1. **Create Database & Table:**

```sql
CREATE DATABASE exampleDB;
USE exampleDB;
CREATE TABLE Employee (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(255),
  email VARCHAR(255) UNIQUE,
  country VARCHAR(255)
);
```

2. **Add JDBC Driver:**
   Download `mysql-connector-java-8.0.33.jar` and add to project libraries.

3. **Set DB credentials** in `DatabaseConnection.java`.

4. **Run** `Main.java` to test CRUD operations.

## Sample Output

```
Inserted employees
Updated by ID, Name, Email
Deleted by ID
Batch Insert: 4 employees added
```

## Future Ideas

* Console input support
* GUI with Swing or JavaFX
* Export to CSV

