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

# 4. Detailed Development Steps

# PHASE 1 — Backend Project Setup

### Step 1 — Verify Java

- [ ] Install Java 25 JDK
- [ ] Verify Java installation
- [ ] Understand JDK vs JRE
- [ ] Configure Java in IntelliJ IDEA

Expected verification:

```text
java -version
```

---

### Step 2 — Verify Maven

- [ ] Install/configure Maven
- [ ] Verify Maven installation
- [ ] Understand Maven
- [ ] Understand `pom.xml`
- [ ] Understand Maven dependencies
- [ ] Understand Maven lifecycle

Expected verification:

```text
mvn -version
```

---

### Step 3 — Create Spring Boot Project

Create the project using Spring Initializr.

Configuration:

```text
Project       → Maven
Language      → Java
Spring Boot   → Spring Boot 4
Java          → 25
Packaging     → Jar
```

Add required dependencies:

```text
Spring Web
Spring Data JPA
MySQL Driver
Lombok
```

Tasks:

- [ ] Create Spring Boot project
- [ ] Open project in IntelliJ IDEA
- [ ] Understand generated files
- [ ] Understand `pom.xml`
- [ ] Run Spring Boot application
- [ ] Verify application starts successfully

---

# PHASE 2 — Backend Project Architecture

### Step 4 — Create Package Structure

Create the following packages:

```text
com.employeemanagement
│
├── entity
├── repository
├── service
├── controller
├── dto
└── exception
```

Tasks:

- [ ] Create `entity`
- [ ] Create `repository`
- [ ] Create `service`
- [ ] Create `controller`
- [ ] Create `dto`
- [ ] Create `exception`

---

### Step 5 — Understand Layered Architecture

Our backend will follow:

```text
Client
  ↓
Controller
  ↓
Service
  ↓
Repository
  ↓
Database
```

Responsibilities:

### Controller

Receives HTTP requests.

```text
GET
POST
PUT
DELETE
```

### Service

Contains application/business logic.

### Repository

Communicates with the database.

### Entity

Represents database data.

### DTO

Transfers data between client and server.

### Exception

Handles errors.

---

# PHASE 3 — Database Setup

### Step 6 — Create MySQL Database

- [ ] Install/configure MySQL
- [ ] Open MySQL Workbench
- [ ] Create database
- [ ] Understand database/schema
- [ ] Configure Spring Boot database connection

Example database:

```text
employee_management
```

---

### Step 7 — Configure `application.properties`

Configure:

```text
Database URL
Database username
Database password
JPA/Hibernate configuration
```

Tasks:

- [ ] Configure MySQL connection
- [ ] Start Spring Boot
- [ ] Verify database connection
- [ ] Understand Hibernate DDL

---

# PHASE 4 — Employee Backend

# Step 8 — Create Employee Entity

Create:

```text
Employee.java
```

The entity will represent an employee record.

Example fields:

```text
id
firstName
lastName
email
```

Tasks:

- [ ] Create Employee class
- [ ] Add `@Entity`
- [ ] Add `@Id`
- [ ] Configure ID generation
- [ ] Add employee fields
- [ ] Generate constructors/getters/setters using Lombok
- [ ] Understand Lombok annotations
- [ ] Run application
- [ ] Verify Employee table

---

# Step 9 — Create Employee Repository

Create:

```text
EmployeeRepository.java
```

Use:

```text
JpaRepository
```

Tasks:

- [ ] Create repository interface
- [ ] Extend `JpaRepository`
- [ ] Understand generic types
- [ ] Understand built-in CRUD methods

Important built-in operations:

```text
save()
findById()
findAll()
deleteById()
```

---

# Step 10 — Create Employee DTO

Create:

```text
EmployeeDTO.java
```

Purpose:

```text
Client
  ↓
EmployeeDTO
  ↓
Service
  ↓
Employee Entity
  ↓
Database
```

Tasks:

- [ ] Create EmployeeDTO
- [ ] Add required fields
- [ ] Understand Entity vs DTO
- [ ] Understand why DTOs are used

---

# PHASE 5 — REST API Development

# Step 11 — Add Employee

Implement:

```text
POST /api/employees
```

Flow:

```text
POST Request
     ↓
EmployeeController
     ↓
EmployeeService
     ↓
EmployeeRepository
     ↓
MySQL
```

Tasks:

- [ ] Create EmployeeService
- [ ] Create EmployeeController
- [ ] Implement POST endpoint
- [ ] Receive EmployeeDTO
- [ ] Convert DTO → Entity
- [ ] Save employee
- [ ] Return response
- [ ] Test using Postman
- [ ] Verify record in MySQL

---

# Step 12 — Get Employee

Implement:

```text
GET /api/employees/{id}
```

Tasks:

- [ ] Create GET endpoint
- [ ] Receive employee ID
- [ ] Find employee using repository
- [ ] Handle employee not found
- [ ] Create ResourceNotFoundException
- [ ] Return EmployeeDTO
- [ ] Test using Postman

Flow:

```text
GET /api/employees/1
          ↓
Controller
          ↓
Service
          ↓
Repository
          ↓
Employee
```

---

# Step 13 — Get All Employees

Implement:

```text
GET /api/employees
```

Tasks:

- [ ] Create get-all service method
- [ ] Use `findAll()`
- [ ] Convert entities to DTOs
- [ ] Return employee list
- [ ] Test using Postman
- [ ] Verify response JSON

Expected concept:

```text
Database
   ↓
List<Employee>
   ↓
List<EmployeeDTO>
   ↓
JSON Response
```

---

# Step 14 — Update Employee

Implement:

```text
PUT /api/employees/{id}
```

Tasks:

- [ ] Receive employee ID
- [ ] Find existing employee
- [ ] Handle employee not found
- [ ] Update fields
- [ ] Save updated employee
- [ ] Return updated employee
- [ ] Test using Postman

Flow:

```text
PUT Request
    ↓
Controller
    ↓
Service
    ↓
Find existing Employee
    ↓
Modify Employee
    ↓
Repository.save()
    ↓
Database
```

---

# Step 15 — Delete Employee

Implement:

```text
DELETE /api/employees/{id}
```

Tasks:

- [ ] Create DELETE endpoint
- [ ] Find employee
- [ ] Handle employee not found
- [ ] Delete employee
- [ ] Return response
- [ ] Test using Postman
- [ ] Verify deletion in MySQL

---

# PHASE 6 — Backend Testing

# Step 16 — Test Complete REST API

Test all operations using Postman.

### Create

```text
POST /api/employees
```

### Read One

```text
GET /api/employees/{id}
```

### Read All

```text
GET /api/employees
```

### Update

```text
PUT /api/employees/{id}
```

### Delete

```text
DELETE /api/employees/{id}
```

Checklist:

- [ ] POST tested
- [ ] GET by ID tested
- [ ] GET all tested
- [ ] PUT tested
- [ ] DELETE tested
- [ ] Invalid ID tested
- [ ] Database verified

---

# PHASE 7 — React Project Setup

# Step 17 — Create React Application

Create the frontend using Vite.

```text
frontend/
```

Tasks:

- [ ] Install Node.js
- [ ] Verify npm
- [ ] Create Vite React application
- [ ] Install dependencies
- [ ] Run React application
- [ ] Open application in browser
- [ ] Understand React project structure

---

# PHASE 8 — React Employee List

# Step 18 — Create List Employee Component

Create the employee list UI.

Tasks:

- [ ] Create ListEmployee component
- [ ] Create employee table
- [ ] Create table columns
- [ ] Create employee state
- [ ] Understand `useState`
- [ ] Understand `useEffect`
- [ ] Display employee data

Initial flow:

```text
React Component
      ↓
Employee State
      ↓
Employee Table
```

---

# PHASE 9 — React Employee Form

# Step 19 — Create Employee Component

Create the form used for:

```text
Add Employee
Update Employee
```

Tasks:

- [ ] Create Employee component
- [ ] Create form
- [ ] Add first name input
- [ ] Add last name input
- [ ] Add email input
- [ ] Add save button
- [ ] Manage form state
- [ ] Handle input changes

---

# PHASE 10 — React Router

# Step 20 — Configure React Router

Create routes for:

```text
/employees
/add-employee
/update-employee/:id
```

Tasks:

- [ ] Install React Router
- [ ] Configure routes
- [ ] Create navigation
- [ ] Navigate to employee list
- [ ] Navigate to add employee
- [ ] Navigate to update employee

---

# PHASE 11 — Form Handling

# Step 21 — Handle Add/Update Form

Use React hooks to manage:

```text
Form data
Input changes
Navigation
URL parameters
```

Tasks:

- [ ] Manage form state
- [ ] Handle input changes
- [ ] Read employee ID from URL
- [ ] Fetch employee for update
- [ ] Populate form
- [ ] Navigate after save

---

# PHASE 12 — Axios API Integration

# Step 22 — Create Axios Services

Create a service layer for API calls.

Example structure:

```text
src/
└── services/
    └── EmployeeService.js
```

Tasks:

- [ ] Install Axios
- [ ] Configure Axios
- [ ] Create employee service
- [ ] Create GET request
- [ ] Create POST request
- [ ] Create PUT request
- [ ] Create DELETE request

Flow:

```text
React Component
       ↓
EmployeeService
       ↓
Axios
       ↓
Spring Boot API
```

---

# PHASE 13 — Connect Employee List

# Step 23 — Fetch Employees From Backend

Connect:

```text
React
  ↓
Axios
  ↓
GET /api/employees
  ↓
Spring Boot
  ↓
MySQL
```

Tasks:

- [ ] Call GET API
- [ ] Receive employee data
- [ ] Store data in state
- [ ] Display employees
- [ ] Test in browser

---

# PHASE 14 — Add Employee From React

# Step 24 — Save Employee

Connect form to:

```text
POST /api/employees
```

Tasks:

- [ ] Collect form data
- [ ] Call Axios POST
- [ ] Send employee data
- [ ] Handle successful response
- [ ] Navigate to employee list
- [ ] Verify database record

---

# PHASE 15 — Update Employee From React

# Step 25 — Dynamic Add/Update Mode

The same Employee component will handle:

```text
Add
```

and

```text
Update
```

based on the URL.

Example:

```text
/add-employee
```

versus:

```text
/update-employee/5
```

Tasks:

- [ ] Detect URL parameter
- [ ] Determine Add vs Update
- [ ] Change page title dynamically
- [ ] Fetch existing employee
- [ ] Populate form
- [ ] Submit update
- [ ] Navigate after update

---

# PHASE 16 — Delete Employee From React

# Step 26 — Delete Employee

Add delete functionality to the employee list.

Flow:

```text
Delete Button
      ↓
Axios DELETE
      ↓
DELETE /api/employees/{id}
      ↓
Spring Boot
      ↓
MySQL
      ↓
Refresh Employee List
```

Tasks:

- [ ] Add Delete button
- [ ] Call DELETE API
- [ ] Handle response
- [ ] Refresh employee list
- [ ] Verify deletion

---

# PHASE 17 — Validation

# Step 27 — Form Validation

Add basic frontend validation.

Tasks:

- [ ] Validate first name
- [ ] Validate last name
- [ ] Validate email
- [ ] Display validation errors
- [ ] Prevent empty submission
- [ ] Test invalid input

---

# PHASE 18 — Bootstrap Styling

# Step 28 — Improve UI

Use Bootstrap to improve the interface.

Tasks:

- [ ] Add Bootstrap
- [ ] Style navbar
- [ ] Style employee table
- [ ] Style employee form
- [ ] Style buttons
- [ ] Add spacing
- [ ] Improve page layout

---

# PHASE 19 — Final Testing

# Step 29 — Test Complete Application

## Create

```text
React Form
    ↓
POST
    ↓
Spring Boot
    ↓
MySQL
```

- [ ] Add employee
- [ ] Verify UI
- [ ] Verify database

## Read

- [ ] View all employees
- [ ] View employee data

## Update

- [ ] Open employee
- [ ] Edit employee
- [ ] Save changes
- [ ] Verify database

## Delete

- [ ] Delete employee
- [ ] Verify UI
- [ ] Verify database

---

# 5. Final Application Architecture

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

# 6. Final Backend Structure

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

# 7. Final Frontend Structure

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

# 8. API Summary

| Method | Endpoint | Purpose |
|---|---|---|
| POST | `/api/employees` | Create employee |
| GET | `/api/employees/{id}` | Get employee |
| GET | `/api/employees` | Get all employees |
| PUT | `/api/employees/{id}` | Update employee |
| DELETE | `/api/employees/{id}` | Delete employee |

---

# 9. Progress Tracker

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