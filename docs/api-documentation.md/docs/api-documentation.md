
# TaskFlow API Documentation

## Overview

This document describes the proposed API for TaskFlow, a sample task management application. The API is designed to allow users and developers to create, retrieve, update, and delete tasks.

**Project Status:** This API is illustrative and is not currently functional.

## Audience

For developers who want to understand how a task management API could be structured and used.

## Base URL

`https://api.taskflow.example/v1`

## Authentication

In a functional implementation, API requests would require an authentication token.

Example:

`Authorization: Bearer YOUR_API_TOKEN`

## Endpoints

### 1. Create a Task

**Endpoint:** `POST /tasks`

Creates a new task.

**Request Body:**

```json
{
  "title": "Complete Anatomy Assignment",
  "description": "Review upper limb anatomy lecture notes",
  "due_date": "2026-11-10"
}
```

**Expected Response:**

```json
{
  "id": 1,
  "title": "Complete Anatomy Assignment",
  "description": "Review upper limb anatomy lecture notes",
  "due_date": "2026-11-10",
  "status": "pending"
}
```

### 2. Retrieve All Tasks

**Endpoint:** `GET /tasks`

Retrieves all tasks associated with the user.

**Expected Response:**

```json
[
  {
    "id": 1,
    "title": "Complete Anatomy Assignment",
    "status": "pending"
  }
]
```

### 3. Retrieve a Single Task

**Endpoint:** `GET /tasks/{id}`

Retrieves a specific task using its ID.

**Example:**

`GET /tasks/1`

### 4. Update a Task

**Endpoint:** `PUT /tasks/{id}`

Updates the details of an existing task.

**Request Body:**

```json
{
  "title": "Complete Anatomy Assignment",
  "status": "completed"
}
```

### 5. Delete a Task

**Endpoint:** `DELETE /tasks/{id}`

Deletes a task using its ID.

**Example:**

`DELETE /tasks/1`

## Status Codes

| Status Code | Description |
|---|---|
| 200 | Request successful |
| 201 | Resource created successfully |
| 400 | Invalid request |
| 401 | Authentication required |
| 404 | Resource not found |
| 500 | Internal server error |

## Error Response Example

```json
{
  "error": "Task not found",
  "status": 404
}
```

## Limitations

TaskFlow is a fictional project. The endpoints, request bodies, and responses in this document are proposed examples and have not been tested against a live API.

## About This Documentation

This API documentation was created as part of a technical writing portfolio project to demonstrate API documentation structure and clarity.

## Accuracy and Edit Note

I reviewed the documentation for clarity, consistency, and formatting. I checked that the endpoint descriptions, request examples, and response examples followed a logical structure. Since TaskFlow is fictional, the API endpoints could not be tested against a functional application.
