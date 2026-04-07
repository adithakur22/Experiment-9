Here’s your cleaned **README.md** (no emojis, trimmed up to Testing section):

---

# JWT Authentication System using Spring Boot

## Project Overview

This project implements a JWT-based authentication system using Spring Boot, Spring Security, and MySQL.
It allows users to log in with credentials and receive a JWT token for secure access to APIs.

---

## Technologies Used

* Java 21
* Spring Boot
* Spring Security
* Spring Data JPA (Hibernate)
* MySQL
* JWT (JSON Web Token)
* Maven

---

## Project Structure

```
com.AML_3B.demo_jwt
│
├── controller
│   └── AuthController.java
│
├── service
│   └── AuthService.java
│
├── repository
│   └── UserRepository.java
│
├── model
│   └── User.java
│
├── security
│   ├── JwtUtil.java
│   └── SecurityConfig.java
│
└── DemoJwtApplication.java
```

---

## Features

* User login using username and password
* JWT token generation
* Secure API access using token
* MySQL database integration

---

## Database Setup

### Create Database:

```sql
CREATE DATABASE jwtdemo;
```

### Table:

```sql
CREATE TABLE users (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255),
    password VARCHAR(255)
);
```

### Insert Sample User:

```sql
INSERT INTO users (username, password) VALUES ('admin', 'admin');
```

---

## Configuration (application.properties)

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/jwtdemo
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

## Running the Application

In Eclipse:

* Right click → Run As → Spring Boot App

---

## API Endpoints

### Login API

```
POST /api/login
```

Headers:

```
Content-Type: application/x-www-form-urlencoded
```

Body:

```
username=admin
password=admin
```

Response:

```
JWT Token (string)
```

---

### Test API

```
GET /api/hello
```

Response:

```
Hello! JWT Authentication Successful
```

---

## How It Works

1. User sends username and password
2. Backend verifies credentials from database
3. If valid, a JWT token is generated
4. Token is returned to the client

---

## Testing (Postman)

Login Request:

* Method: POST
* URL: [http://localhost:8080/api/login](http://localhost:8080/api/login)
* Body: x-www-form-urlencoded

| Key      | Value |
| -------- | ----- |
| username | admin |
| password | admin |

---

<img width="1731" height="788" alt="Screenshot 2026-04-07 145808" src="https://github.com/user-attachments/assets/2563f3cb-6e03-47e1-b8f3-e0983b62b19f" />
<img width="1085" height="606" alt="Screenshot 2026-04-07 150715" src="https://github.com/user-attachments/assets/8f7d01e4-9ce8-418d-9dce-86f595e23ddc" />
<img width="1092" height="847" alt="Screenshot 2026-04-07 150623" src="https://github.com/user-attachments/assets/bbfa6909-d2b8-4ce9-964d-c7f2ba394f1c" />


