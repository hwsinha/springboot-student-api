# Student Management REST API

A RESTful Student Management API built with **Spring Boot**, **Spring Data JPA**, **Hibernate**, and **MySQL**. The application demonstrates CRUD operations following a layered architecture (Controller → Service → Repository) and includes support for **Soft Delete**.

---

## Features

- Create a Student
- Retrieve Student by ID
- Retrieve All Students
- Update Student Details
- Permanently Delete a Student
- Soft Delete (Logical Delete)
- RESTful API
- MySQL Database Integration
- Layered Architecture

---

## Tech Stack

- Java 21
- Spring Boot
- Spring Data JPA
- Hibernate ORM
- MySQL
- Maven

---

## Project Structure

```
springboot-student-api
├── .idea
├── .mvn
├── src
│   ├── main
│   │   ├── java
│   │   │   └── in.strikes.crudSpringBootDemo
│   │   │       ├── controller
│   │   │       ├── entity
│   │   │       ├── repository
│   │   │       ├── service
│   │   │       └── CrudSpringBootDemoApplication.java
│   │   └── resources
│   │       └── application.properties
│   └── test
├── pom.xml
└── ...
```

---


## API Endpoints

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | `/api/students/create` | Create a new student |
| GET | `/api/students/get?id={id}` | Retrieve a student by ID |
| GET | `/api/students/getAll` | Retrieve all active students |
| PUT | `/api/students/update?id={id}` | Update student details |
| DELETE | `/api/students/delete?id={id}` | Permanently delete a student |
| PATCH | `/api/students/delete-soft?id={id}` | Soft delete a student |

---

## Database Configuration

Create a MySQL database:

```sql
CREATE DATABASE student_crud_db;
```

Update your local database credentials in `application.properties`.

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/student_crud_db
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD
```

---

## Running the Project

Clone the repository:

```bash
git clone https://github.com/hwsinha/springboot-student-api.git
```

Navigate to the project:

```bash
cd springboot-student-api
```

Run the application:

```bash
./mvnw spring-boot:run
```

or

```bash
mvn spring-boot:run
```

The application will start on:

```
http://localhost:8080
```

---

## Soft Delete

Instead of permanently removing records, the application also supports **Soft Delete** by updating a `deleted` flag. Soft deleted records are excluded from retrieval operations while remaining stored in the database.

---

## Sample Student JSON

```json
{
  "name": "Harshwardhan Sinha",
  "age": 21,
  "email": "harshwar.sinha@gmail.com",
  "rollNo": 143,
  "subject": "Spring Boot"
}
```

---


## Author

**Harshwardhan Sinha**

GitHub: https://github.com/hwsinha