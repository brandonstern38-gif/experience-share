# API Specification

## Overview
This document outlines the REST API endpoints for the Experience Share application.

## Base URL
`https://api.example.com/v1`

## Endpoints

### 1. GET /users
- **Description**: Retrieve a list of users.
- **Response**:
  - `200 OK`: List of users.
  - `404 Not Found`: No users found.

### 2. GET /users/{id}
- **Description**: Retrieve a user by ID.
- **Parameters**:
  - **id** (path): Unique identifier for the user.
- **Response**:
  - `200 OK`: User object.
  - `404 Not Found`: User not found.

### 3. POST /users
- **Description**: Create a new user.
- **Request Body**:
  - `name`: User's name.
  - `email`: User's email.
- **Response**:
  - `201 Created`: User created successfully.
  - `400 Bad Request`: Invalid input.

### 4. PUT /users/{id}
- **Description**: Update an existing user.
- **Parameters**:
  - **id** (path): Unique identifier for the user.
- **Request Body**:
  - `name`: User's new name.
  - `email`: User's new email.
- **Response**:
  - `200 OK`: User updated successfully.
  - `404 Not Found`: User not found.

### 5. DELETE /users/{id}
- **Description**: Delete a user by ID.
- **Parameters**:
  - **id** (path): Unique identifier for the user.
- **Response**:
  - `204 No Content`: User deleted successfully.
  - `404 Not Found`: User not found.

## Conclusion
This API provides a structured way to interact with the Experience Share application. Ensure to handle error responses appropriately in your applications.