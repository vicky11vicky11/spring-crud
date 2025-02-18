# User Management CRUD App

This is a simple User Management CRUD application built using React for the frontend and Spring Boot for the backend.

## Features
- Create, Read, Update, and Delete (CRUD) users
- Responsive design using CSS Grid
- REST API integration

## API Endpoints

### Base URL
```
http://localhost:8080/api
```

### 1. Get All Users
**Endpoint:**
```
GET /users
```
**Response:**
```json
[
  {
    "id": 1,
    "username": "johndoe",
    "name": "John Doe",
    "email": "johndoe@example.com"
  },
  {
    "id": 2,
    "username": "janedoe",
    "name": "Jane Doe",
    "email": "janedoe@example.com"
  }
]
```

### 2. Get User by ID
**Endpoint:**
```
GET /user/{id}
```
**Response:**
```json
{
  "id": 1,
  "username": "johndoe",
  "name": "John Doe",
  "email": "johndoe@example.com"
}
```

### 3. Create a New User
**Endpoint:**
```
POST /user
```
**Request Body:**
```json
{
  "username": "newuser",
  "name": "New User",
  "email": "newuser@example.com"
}
```
**Response:**
```json
{
  "id": 3,
  "username": "newuser",
  "name": "New User",
  "email": "newuser@example.com"
}
```

### 4. Update a User
**Endpoint:**
```
PUT /user/{id}
```
**Request Body:**
```json
{
  "username": "updateduser",
  "name": "Updated User",
  "email": "updateduser@example.com"
}
```
**Response:**
```json
{
  "id": 1,
  "username": "updateduser",
  "name": "Updated User",
  "email": "updateduser@example.com"
}
```

### 5. Delete a User
**Endpoint:**
```
DELETE /user/{id}
```
**Response:**
```
"User deleted successfully"
```

### 6. Add Multiple Users
**Endpoint:**
```
POST /users
```
**Request Body:**
```json
[
  {
    "username": "user1",
    "name": "User One",
    "email": "user1@example.com"
  },
  {
    "username": "user2",
    "name": "User Two",
    "email": "user2@example.com"
  }
]
```
**Response:**
```json
[
  {
    "id": 4,
    "username": "user1",
    "name": "User One",
    "email": "user1@example.com"
  },
  {
    "id": 5,
    "username": "user2",
    "name": "User Two",
    "email": "user2@example.com"
  }
]
```

## How to Run
1. Start the Spring Boot backend on port `8080`.
2. Run the React frontend using:
   ```sh
   npm install
   npm start
   ```
3. Open `http://localhost:3000/` in your browser.

## Tech Stack
- **Frontend:** React, React Router, Axios
- **Backend:** Spring Boot, Spring Data JPA
- **Database:** MySQL

