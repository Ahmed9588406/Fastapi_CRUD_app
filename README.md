# Fastapi_CRUD_app

Here's a sample README file for your FastAPI project on GitHub:

**Task Management API**
=====================

This is a simple task management API built using FastAPI. It allows users to create, read, update, and delete tasks.

**Endpoints**
------------

### Create Task

* **POST /tasks/**
	+ Request Body: `Task` object with `title`, `description`, and `completed` fields
	+ Response: Created `Task` object with generated `id`

### Read Tasks

* **GET /tasks/**
	+ Response: List of all `Task` objects

### Read Task

* **GET /tasks/{task_id}**
	+ Path Parameter: `task_id` (UUID)
	+ Response: `Task` object with the specified `id`

### Update Task

* **PUT /tasks/{task_id}**
	+ Path Parameter: `task_id` (UUID)
	+ Request Body: `Task` object with updated fields
	+ Response: Updated `Task` object

### Delete Task

* **DELETE /tasks/{task_id}**
	+ Path Parameter: `task_id` (UUID)
	+ Response: Deleted `Task` object

**Models**
---------

### Task

* `id`: UUID (generated automatically)
* `title`: String (required)
* `description`: String (optional)
* `completed`: Boolean (default: False)

**Running the API**
-----------------

To run the API, execute the following command:

```
uvicorn main:app --host 0.0.0.0 --port 8000
```

Replace `main` with the name of your Python file containing the FastAPI application.

**Testing the API**
-----------------

You can use tools like `curl` or a REST client (e.g., Postman) to test the API endpoints.
