Spring Framework Application – Task 2 (REST API)

This repository contains a Spring Boot REST API application developed as Task 2 for the Spring Framework Apps – Projects for Everyone course at Akademia Finansów i Biznesu Vistula.

The project demonstrates a complete backend REST application built using Spring Boot, following clean layered architecture, REST principles, proper exception handling, API documentation with Swagger, and database persistence using Spring Data JPA and H2.

------

📌 Task 2 – REST API with Spring Boot
🎯 Objective

The objective of Task 2 is to design and implement a RESTful backend application that:

Exposes REST endpoints using standard HTTP methods

Applies layered architecture (Controller, Service, Repository)

Uses DTOs and object mapping

Implements centralized exception handling

Documents APIs using Swagger / OpenAPI

Persists data using Spring Data JPA and an H2 in-memory database

-----

🛠️ Technologies Used

Java

Spring Boot

Spring Web

Spring Data JPA

H2 Database

Swagger / OpenAPI

Maven

Postman

Hibernate

-----

🏗️ Application Architecture

The application follows a layered architecture:

Controller → Service → Repository → Database

Application Flow

Client sends an HTTP request in JSON format

Controller receives the request and maps it to a DTO

Service layer processes business logic

Repository interacts with the database

Mapper converts Entities ↔ DTOs

Controller returns an HTTP response with appropriate status

-----

📡 REST API Endpoints
Method	Endpoint	Description	HTTP Status
POST	/api/v1/products	Create a new product	201 Created
GET	/api/v1/products/{id}	Get product by ID	200 OK
GET	/api/v1/products	Get all products	200 OK
PUT	/api/v1/products/{id}	Update product	200 OK
DELETE	/api/v1/products/{id}	Delete product	204 No Content

🧾 Example JSON Requests
Create Product (POST)
{
  "name": "Laptop"
}

Update Product (PUT)
{
  "name": "MacBook"
}

-----

❗ Exception Handling

Custom exception: ProductNotFoundException

Centralized exception handling using @ControllerAdvice

Proper HTTP status codes returned (e.g. 404 NOT FOUND)

Error responses wrapped in a structured ErrorMessageResponse

-----

📘 API Documentation (Swagger / OpenAPI)

Swagger UI is enabled for interactive API documentation and testing.

Swagger UI:
http://localhost:8080/swagger-ui/index.html

OpenAPI JSON:
http://localhost:8080/v1/api-docs

-----

🗄️ Database Integration (H2 + JPA)

In-memory H2 database

Hibernate automatically generates database tables

Entity mapping using:

@Entity

@Id

@GeneratedValue

Repository extends JpaRepository<Product, Long>

H2 Console

URL: http://localhost:8080/console

JDBC URL: jdbc:h2:mem:testdb

-----

🧪 Testing

The REST endpoints were tested using:

Swagger UI

Postman

Browser (GET requests)

Test Coverage

Full CRUD operations

Valid and invalid input cases

Exception handling for non-existing product IDs

-----

📌 Final Notes

The project is version-controlled using Git

.gitignore is included to exclude unnecessary files

The application is ready for live demonstration and testing

The solution follows Spring Boot and REST best practices
