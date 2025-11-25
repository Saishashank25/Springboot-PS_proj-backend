# Finance Tracker Backend

This repository contains the backend service for a personal finance tracking application, built with Java and the Spring Boot framework.

## Technologies Used

*   **Framework:** Spring Boot 3.5.0
*   **Language:** Java 17
*   **Database:** Spring Data JPA with MySQL
*   **Security:** Spring Security, JSON Web Tokens (JWT)
*   **Build Tool:** Apache Maven
*   **Testing:** JUnit 5

## Prerequisites

Before you begin, ensure you have the following installed on your system:
*   JDK 17 or later
*   Apache Maven (or you can use the included Maven Wrapper)
*   A running instance of MySQL server

## Getting Started

Follow these instructions to get a local copy up and running.

### 1. Clone the Repository

```sh
git clone https://github.com/saishashank25/springboot-ps_proj-backend.git
cd springboot-ps_proj-backend
```

### 2. Configure the Database

This project uses MySQL. You need to configure the database connection.

1.  Create a new file named `application.properties` in the `src/main/resources` directory.
2.  Add your database configuration to this file. Replace the placeholder values (`your_database_name`, `your_username`, `your_password`) with your actual MySQL credentials.

**`src/main/resources/application.properties`:**
```properties
# MySQL Database Configuration
spring.datasource.url=jdbc:mysql://localhost:3306/your_database_name
spring.datasource.username=your_username
spring.datasource.password=your_password

# JPA/Hibernate Configuration
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect

# Server Port (Optional)
server.port=8080
```

### 3. Build the Project

You can build the project using the included Maven Wrapper. This will download all necessary dependencies.

On macOS/Linux:
```sh
./mvnw clean install
```
On Windows:
```sh
./mvnw.cmd clean install
```

### 4. Run the Application

Once the project is built, you can run the application with the following command.

On macOS/Linux:
```sh
./mvnw spring-boot:run
```
On Windows:
```sh
./mvnw.cmd spring-boot:run
```

The application will start, and the backend server will be running on `http://localhost:8080`.
