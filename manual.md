# CRUD API with Express - Manual

This document provides instructions on how to set up, run, and use the CRUD API.

## 1. Installation

First, you need to install the project dependencies. Open your terminal in the project root directory and run the following command:

```bash
npm install
```

This will install Express.js, body-parser, and the Swagger packages.

## 2. Running the Server

To start the API server, run the following command from the project root:

```bash
node index.js
```

You should see the following output, indicating that the server is running:

```
Server is running on http://localhost:3000
Swagger docs available at http://localhost:3000/api-docs
```

## 3. API Endpoints

The API provides the following endpoints to manage users. You can use tools like `curl` or Postman to interact with them.

### GET /users
Returns a list of all users.

**Example using `curl`:**
```bash
curl http://localhost:3000/users
```

### GET /users/:id
Returns a single user by their ID.

**Example using `curl`:**
```bash
curl http://localhost:3000/users/1
```

### POST /users
Creates a new user. You need to provide the user's name and email in the request body.

**Example using `curl`:**
```bash
curl -X POST -H "Content-Type: application/json" -d '{"name": "New User", "email": "new.user@example.com"}' http://localhost:3000/users
```

### PUT /users/:id
Updates an existing user's information.

**Example using `curl`:**
```bash
curl -X PUT -H "Content-Type: application/json" -d '{"name": "Updated User", "email": "updated.user@example.com"}' http://localhost:3000/users/1
```

### DELETE /users/:id
Deletes a user by their ID.

**Example using `curl`:**
```bash
curl -X DELETE http://localhost:3000/users/1
```

## 4. Swagger Documentation

For interactive API documentation, open your web browser and navigate to:

[http://localhost:3000/api-docs](http://localhost:3000/api-docs)

Here, you can view all the endpoints and even test them directly from your browser.
