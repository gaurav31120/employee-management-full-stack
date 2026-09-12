# Employee Management System

A Full-Stack Employee Management System built using **Spring Boot, Java, MySQL, React, Axios, React Router, and Bootstrap**.

This project follows the development flow of the reference lecture while being implemented and understood step-by-step.

---

# 1. Tech Stack

## Backend

| Technology | Purpose |
|---|---|
| Java 25 | Backend programming language |
| Spring Boot 4 | Backend framework |
| Spring Web | Building REST APIs |
| Spring Data JPA | Database operations |
| Hibernate | ORM / JPA implementation |
| Maven | Build and dependency management |
| Lombok | Reducing boilerplate Java code |
| MySQL | Relational database |

## Frontend

| Technology | Purpose |
|---|---|
| React 18 | Frontend library |
| JavaScript | Frontend programming |
| Vite | React project/build tool |
| Axios | HTTP/API communication |
| React Router | Frontend routing |
| Bootstrap | UI styling |
| HTML/CSS | Structure and styling |

## Development Tools

| Tool | Purpose |
|---|---|
| IntelliJ IDEA | Backend development |
| VS Code | Frontend development |
| MySQL | Database |
| MySQL Workbench | Database management |
| Postman | REST API testing |
| Git | Version control |
| GitHub | Remote repository |

---

# 2. Project Structure

```text
employee-management/
│
├── backend/
│
├── frontend/
│
├── database/
│
├── README.md
│
└── .gitignore
```

The project will initially contain only the major sections.

The internal backend/frontend structure will be created gradually as we progress through the development steps.

---

# 3. Overall Development Flow

```text
Project Setup
      ↓
Spring Boot Backend Setup
      ↓
Backend Architecture
      ↓
Employee Entity
      ↓
Repository
      ↓
DTO
      ↓
Create Employee API
      ↓
Get Employee API
      ↓
Get All Employees API
      ↓
Update Employee API
      ↓
Delete Employee API
      ↓
Test Backend APIs
      ↓
React + Vite Setup
      ↓
React Components
      ↓
Employee List UI
      ↓
Employee Form UI
      ↓
React Router
      ↓
Form Handling
      ↓
Axios Services
      ↓
Backend ↔ Frontend Integration
      ↓
Add Employee
      ↓
Update Employee
      ↓
Delete Employee
      ↓
Validation
      ↓
Final Testing
```

---



# 4. Final Application Architecture

```text
                         USER
                           │
                           ▼
                  ┌─────────────────┐
                  │      React      │
                  │    Frontend     │
                  └────────┬────────┘
                           │
                       Axios HTTP
                           │
                           ▼
                  ┌─────────────────┐
                  │   Spring Boot   │
                  │    Controller   │
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │     Service     │
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │    Repository   │
                  └────────┬────────┘
                           │
                       Hibernate
                           │
                           ▼
                  ┌─────────────────┐
                  │      MySQL      │
                  └─────────────────┘
```

---

# 5. Final Backend Structure

After completing the backend portion:

```text
backend/
│
├── src/
│   └── main/
│       ├── java/
│       │   └── com/
│       │       └── employeemanagement/
│       │           │
│       │           ├── EmployeeManagementApplication.java
│       │           │
│       │           ├── entity/
│       │           │   └── Employee.java
│       │           │
│       │           ├── repository/
│       │           │   └── EmployeeRepository.java
│       │           │
│       │           ├── service/
│       │           │   └── EmployeeService.java
│       │           │
│       │           ├── controller/
│       │           │   └── EmployeeController.java
│       │           │
│       │           ├── dto/
│       │           │   └── EmployeeDTO.java
│       │           │
│       │           └── exception/
│       │               └── ResourceNotFoundException.java
│       │
│       └── resources/
│           └── application.properties
│
└── pom.xml
```

---

# 6. Final Frontend Structure

After completing the frontend portion:

```text
frontend/
│
├── public/
│
├── src/
│   │
│   ├── components/
│   │   ├── ListEmployee.jsx
│   │   └── Employee.jsx
│   │
│   ├── services/
│   │   └── EmployeeService.js
│   │
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
│
├── package.json
└── vite.config.js
```

---

# 7. API Summary

| Method | Endpoint | Purpose |
|---|---|---|
| POST | `/api/employees` | Create employee |
| GET | `/api/employees/{id}` | Get employee |
| GET | `/api/employees` | Get all employees |
| PUT | `/api/employees/{id}` | Update employee |
| DELETE | `/api/employees/{id}` | Delete employee |

---

# 8. Progress Tracker

## Backend

- [ ] Java & Maven setup
- [ ] Spring Boot project
- [ ] Dependencies
- [ ] Package architecture
- [ ] MySQL configuration
- [ ] Employee Entity
- [ ] Employee Repository
- [ ] Employee DTO
- [ ] Employee Service
- [ ] Employee Controller
- [ ] POST API
- [ ] GET by ID API
- [ ] GET all API
- [ ] PUT API
- [ ] DELETE API
- [ ] Exception handling
- [ ] Postman testing

## Frontend

- [ ] Node.js/npm setup
- [ ] Vite React project
- [ ] List Employee component
- [ ] Employee component
- [ ] React state
- [ ] React hooks
- [ ] React Router
- [ ] Form handling
- [ ] Axios
- [ ] GET integration
- [ ] POST integration
- [ ] PUT integration
- [ ] DELETE integration
- [ ] Validation
- [ ] Bootstrap styling
- [ ] Final testing

---

# 10. Learning Checkpoint

After each major step, I should be able to explain:

### Backend

```text
What is Spring Boot?
What is Maven?
What is JPA?
What is Hibernate?
What is an Entity?
What is JpaRepository?
What is a DTO?
What is a Service?
What is a Controller?
What is REST?
What is POST?
What is GET?
What is PUT?
What is DELETE?
```

### Frontend

```text
What is React?
What is Vite?
What is a component?
What is JSX?
What is state?
What is useState?
What is useEffect?
What is React Router?
What is Axios?
How does React call Spring Boot?
```

---

# 11. Development Rule

We will follow the lecture sequence.

For every development step:

```text
1. Understand the concept
        ↓
2. Create the required file
        ↓
3. Write the code
        ↓
4. Understand the code
        ↓
5. Run the application
        ↓
6. Test the feature
        ↓
7. Fix errors if any
        ↓
8. Mark README task as DONE
        ↓
9. Commit the changes
        ↓
10. Move to the next step
```

We will **not jump ahead to advanced technologies** until the basic Employee Management application is complete.

---

# 12. Current Status

```text
Project Setup     ⬜
Backend           ⬜
Database          ⬜
REST APIs         ⬜
Postman Testing   ⬜
React             ⬜
Axios             ⬜
React Router      ⬜
CRUD UI           ⬜
Validation        ⬜
Styling           ⬜
Final Testing     ⬜
```

**Current Step: 1 — Project Setup**