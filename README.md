# Customer API for Dunder Mifflin Paper Store
This is a Customer Management API built with Spring Boot. The API allows users to _Create, View, List and Delete_ customers for the Dunder Mifflin Paper Store. This API is designed to showcase good code structure, simplicity in solving problems, and best practices for documentation and testing.
_______________________________________________________________________________________________

**Features**
+ **Create** new customers
+ **View** an individual customer by ID
+ **List** all customers
+ **Delete** a customer by ID

**Project Structure**
The project is organized into the following layers:
+ **Model:** Defines the _Customer_ entity
+ **Repository:** Interface for database operations extending _JpaRepository_ (CRUD methods are inherited).
+ **Service:** Contains business logic and interacts with the repository.
+ **Controller:** Handles HTTP requests and maps them to service layer methods.
_______________________________________________________________________________________________

**Technologies Used**
+ **Java 11**
+ **Spring Boot**
+ **Spring Data JPA**
+ **H2 Database**
+ **Maven**
_______________________________________________________________________________________________

**Getting started**
Follow these instructions to run the project locally

**Prerequisites**
+ **Java 11** or higher
+ **Maven** installed on your system
**Clone the repository**

_git clone  https://github.com/sarazvi/CustomerAPI/_

_cd CustomerAPI_


**Build and Run the project**

You can build the project using Maven:

_mvn clean install_

To run the project:

bash

Copy code

_mvn spring-boot:run_

This will start the application and host it on _http://localhost:8080_
_______________________________________________________________________________________________

**API Endpoints**

**Base URL**

All requests should be made to:

_http://localhost:8080/api/customers_

**1. Get All Customers**
+ **Endpoint:** _GET /api/customers_
+ **Description:** Retrieves a list of all customers.
+ **Response:** Array of customer object.
**Example Request:**
_curl -X GET http://localhost:8080/api/customers_

**2. Get Customer by ID**
+ **Endpoint:** GET /api/customers/{id}
+ **Description:** Retrieves a customer by their ID.
+ **Response:** A customer object if found, otherwise 4040 Not Found.
**Example Request:**
  _curl -X GET http://localhost:8080/api/customers/1_

**3. Create a Customer**
+ **Endpoint:** _POST /api/customers_
+ **Description:** Creates a new customer.
+ **Request Body:**

  {
  "name": "John Doe",
  "email": "john@example.com"
  }
+ **Response:** The created customer object.
  **Example Request:**

  _curl -X POST http://localhost:8080/api/customers \
  -H "Content-Type: application/json" \
  -d '{"name": "John Doe", "email": "john@example.com"}_

**4. Delete a Customer**
+ **Endpoint:** _DELETE /api/customers/{id}
+ **Description:** Deletes a customer by their ID.
+ **Response:** 204 No Content if successful, otherwise 404 Not Found.

**Example Request:**

 _curl -X DELETE http://localhost:8080/api/customers/1_
_______________________________________________________________________________________________

**Testing the API**
You can test the API using Postman or cURL.
Alternatively, you can enable the H2 database console for in-memory inspection by visiting:

_http://localhost:8080/h2-console_

Use the following credentials to log in:
+ **JDBC URL:** _jdbc:h2:mem:testdb_
+ **Username:** sa
+ **Password:** password
_______________________________________________________________________________________________

**How to Contribute**
Feel free to fork this project and create a pull request to contribute to its development. For major changes, please open an issue first to discuss what you would like to change.
_______________________________________________________________________________________________

**Author**
+ Salma Razvi
+ razvisalma070@gmail.com


  
