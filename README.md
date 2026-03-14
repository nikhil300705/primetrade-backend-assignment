# Primetrade Backend Developer Assignment

## Overview

This project implements a secure and scalable backend system with authentication, role-based access control, and CRUD operations.
A simple frontend interface is also included to test and interact with the APIs.

The goal of this project is to demonstrate backend architecture, API design, authentication security, and database integration.

---

## Tech Stack

Backend

* Node.js
* Express.js
* MongoDB
* Mongoose
* JWT Authentication
* bcrypt for password hashing

Frontend

* HTML
* CSS
* Vanilla JavaScript (Fetch API)

---

## Project Structure

```
primetrade-backend-assignment
│
├── primetrade-backend-task
│   ├── backend
│   │   ├── config
│   │   │   └── db.js
│   │   ├── controllers
│   │   │   ├── authController.js
│   │   │   └── taskController.js
│   │   ├── middleware
│   │   │   ├── authMiddleware.js
│   │   │   └── roleMiddleware.js
│   │   ├── models
│   │   │   ├── User.js
│   │   │   └── Task.js
│   │   ├── routes
│   │   │   ├── authRoutes.js
│   │   │   └── taskRoutes.js
│   │   ├── utils
│   │   └── server.js
│   │
│   └── frontend
│       └── index.html
│
└── README.md
```

---

## Features Implemented

### Authentication

* User Registration
* User Login
* Password hashing using bcrypt
* JWT based authentication

### Role-Based Access Control

* Two roles supported
* User
* Admin
* Middleware to restrict protected routes

### Task Management (CRUD APIs)

Users can manage tasks with the following operations:

* Create Task
* Get Tasks
* Update Task
* Delete Task

### API Versioning

All APIs are versioned:

```
/api/v1/
```

Example:

```
/api/v1/auth/register
/api/v1/auth/login
/api/v1/tasks
```

---

## API Endpoints

### Authentication

Register User

POST /api/v1/auth/register

Example Request

```
{
"name": "Nikhil",
"email": "nikhil@gmail.com",
"password": "123456"
}
```

Login User

POST /api/v1/auth/login

Example Request

```
{
"email": "nikhil@gmail.com",
"password": "123456"
}
```

Response

```
{
"token": "JWT_TOKEN"
}
```

---

### Task APIs

Create Task

POST /api/v1/tasks

Headers

```
Authorization: Bearer <JWT_TOKEN>
```

Body

```
{
"title": "Backend Assignment",
"description": "Complete API implementation"
}
```

---

Get All Tasks

GET /api/v1/tasks

---

Update Task

PUT /api/v1/tasks/:id

---

Delete Task

DELETE /api/v1/tasks/:id

---

## Frontend UI

A simple UI is included to interact with APIs.

Features

* Register user
* Login user
* Create tasks
* View tasks

Frontend File

```
frontend/index.html
```

---

## Running the Project

### Clone Repository

```
git clone https://github.com/nikhil300705/primetrade-backend-assignment.git
```

---

### Install Dependencies

```
cd primetrade-backend-task/backend
npm install
```

---

### Start Server

```
npm run dev
```

Server runs on

```
http://localhost:8000
```

---

### Open Frontend

Open the following file in browser

```
frontend/index.html
```

---

## Security Practices

* Password hashing using bcrypt
* JWT token authentication
* Protected routes using middleware
* Role-based access control
* Input validation

---

## Scalability Considerations

The project structure allows easy scalability.

Possible improvements:

* Add Redis caching
* Add logging (Winston / Morgan)
* Dockerize the application
* Implement rate limiting
* Split into microservices architecture

---

## Author

Nikhil Eswar

GitHub
https://github.com/nikhil300705
