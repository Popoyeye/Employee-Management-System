# Employee-Management-System
A Spring Boot-based REST API for managing employee information, built with Spring Data JPA, Hibernate, and MySQL. This project serves as a backend service that provides CRUD operations for managing employee records.

Technology Used :

Java : 21

Spring Boot : 3.40

Spring Data JPA : For ORM functionality

Hibernate : For database interactions

MySQL : Database

IntelliJ IDEA : Development environment

Project Structure : 

The application is organized as follows :

src

├── main

│   ├── java

│   │   └── com.example.ems_backend

│   │       ├── controller             // REST API Controllers: Handles HTTP requests and directs them to the appropriate service layer.

│   │       ├── dto                    // Data Transfer Objects (DTO): Used to transfer data between layers and optimize data serialization.

│   │       ├── entity                 // Entity Classes: Represents the database entities and is mapped to the database tables.

│   │       ├── repository             // JPA Repositories: Interfaces extending JpaRepository for database operations.

│   │       ├── service                // Service Classes: Contains business logic and operations.

│   │       │   └── impl               // Implementation Classes: Provides concrete implementations of service interfaces.

│   │       ├── exception              // Custom Exceptions: Defines specific exceptions for the application.

│   │       ├── mapper                 // Mapper Classes: Transforms entities to DTOs and vice versa.

│   │       └── EmployeeManagementApplication.java // Main Application Class: Entry point of the Spring Boot application.

│   └── resources

│       └── application.properties     // Configuration file: Contains application settings, such as database configurations.

Setup and Installation : 

1) Clone the repository:
   
	git clone https://github.com/your-username/employee-management.git

	cd employee-management

2) Open in IntelliJ IDEA:

	 Import the project as a Maven project in IntelliJ IDEA.

3) Install dependencies:

	 All dependencies are managed via Maven, so they will be downloaded automatically.

Database Configuration : 

1) Create MySQL Database:

   CREATE DATABASE employee_management;

2) Update application.properties:

   spring.datasource.url=jdbc:mysql://localhost:3306/employee_management
   
	 spring.datasource.username=your_mysql_username

	 spring.datasource.password=your_mysql_password

	 spring.jpa.hibernate.ddl-auto=update

	 spring.jpa.show-sql=true

Running the Application : 

1) Run the main class:

	 Open EmployeeManagementApplication.java and run the main method to start the application.

2) Access the API:

   Once the application starts, you can access the API at

   http://localhost:8080/api/employees.

API Endpoints : 

The following endpoints are available for managing employees:
 
| Method        | Endpoint              | Description           |
| ------------- |:---------------------:| ---------------------:|
| GET           | /api/employees        | Get all employees     |
| GET           | /api/employees/{id}   | Get employee by ID    |
| POST          | /api/employees        | Add a new employee    |
| DELETE        | /api/employees/{id}   | Delete employee by ID |
| PUT           | /api/employees/{id}   | Update employee by ID |






