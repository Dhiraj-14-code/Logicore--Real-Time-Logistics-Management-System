# 🚚 LogiCore — Real-Time Logistics Management System

**LogiCore** is a logistics management platform designed to simplify shipment management, monitor delivery progress, and improve logistics operations through a structured and scalable application architecture.

The project is being developed using Java, Spring Boot, MySQL, and React.

## 🎯 Project Objectives

- Manage shipment records efficiently.
- Track shipment status throughout the delivery lifecycle.
- Prevent duplicate tracking numbers.
- Validate shipment status transitions.
- Provide structured API responses and centralized exception handling.
- Build a maintainable backend architecture.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Java 21 | Backend programming |
| Spring Boot | Backend framework |
| Spring Data JPA | Database operations |
| Hibernate | ORM |
| MySQL | Relational database |
| Maven | Dependency management |
| Lombok | Boilerplate reduction |
| Git & GitHub | Version control |
| React + Vite | Frontend (planned) |
| Postman | API testing |

## 🏗️ Backend Architecture

The application follows a layered architecture:

```text
Client
  |
Controller Layer
  |
Service Layer
  |
Mapper Layer
  |
Repository Layer
  |
MySQL Database
```

### Package Structure

```text
src/main/java/com/logicore/Logicore/
│
├── dto/
│   ├── ShipmentRequestDTO.java
│   └── ShipmentResponseDTO.java
│
├── entity/
│   └── Shipment.java
│
├── enums/
│   ├── ShipmentStatus.java
│   └── ShipmentPriority.java
│
├── exception/
│   ├── ResourceNotFoundException.java
│   ├── DuplicateResourceException.java
│   ├── InvalidStatusTransitionException.java
│   ├── ErrorResponse.java
│   └── GlobalExceptionHandler.java
│
├── mapper/
│   └── ShipmentMapper.java
│
├── repository/
│   └── ShipmentRepository.java
│
└── service/
    └── ShipmentService.java
```

## ✅ Implemented Features

- Shipment creation and retrieval.
- Shipment update and deletion.
- Search shipment by ID.
- Duplicate tracking-number validation.
- Shipment status management.
- Shipment status transition validation.
- Custom exception classes.
- Centralized exception handling.
- Structured error response DTO.

## 📦 Shipment Status Lifecycle

```text
CREATED
   |
PICKED_UP
   |
IN_TRANSIT
   |
OUT_FOR_DELIVERY
   |
DELIVERED
```

Shipment cancellation is also supported where permitted by the business rules.

Invalid status transitions are rejected by the service layer.

## 🗺️ Development Roadmap

- [x] Project initialization and database configuration
- [x] Shipment entity, enums and DTOs
- [x] Mapper and repository
- [x] Basic shipment CRUD service methods
- [x] Duplicate tracking-number validation
- [x] Shipment status transition validation
- [x] Custom exceptions
- [x] Global exception handling
- [ ] Complete validation error responses
- [ ] REST API controllers
- [ ] API testing with Postman
- [ ] Pagination, sorting and filtering
- [ ] Shipment tracking history
- [ ] Delivery-agent management
- [ ] Spring Security and JWT authentication
- [ ] React frontend integration
- [ ] Testing and deployment

## ⚙️ Getting Started

### Prerequisites

- Java 21
- Maven
- MySQL
- IntelliJ IDEA or another Java IDE

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/LogiCore.git
```

### 2. Navigate to the project

```bash
cd LogiCore
```

### 3. Create the MySQL database

```sql
CREATE DATABASE logicore_db;
```

### 4. Configure database credentials

Update your local `application.properties` with your MySQL configuration.

Do not commit database passwords or other sensitive credentials to GitHub.

### 5. Run the application

```bash
mvn spring-boot:run
```

## 🎓 Learning Outcomes

This project is also an opportunity to strengthen practical knowledge of:

- Object-Oriented Programming in Java.
- Layered application architecture.
- REST API development.
- DTO and entity mapping.
- Spring Dependency Injection.
- Spring Data JPA and Hibernate.
- Business logic implementation.
- Exception handling and validation.
- Database design and integration.

## 👨‍💻 Author

**Dhiraj**

Information Technology Engineering Student

---

*LogiCore is an ongoing development project. Features will be added incrementally as the backend and frontend evolve.*
