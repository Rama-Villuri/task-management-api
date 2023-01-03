# task-management-api

# task-management-api

# Task Management API

This API allows users to create, edit, and delete tasks, as well as organize them into lists.

## Endpoints

The following endpoints are available:

### Tasks

- `GET /tasks`: Retrieve a list of tasks
- `GET /tasks/{id}`: Retrieve a specific task
- `POST /tasks`: Create a new task
- `PUT /tasks/{id}`: Update an existing task
- `DELETE /tasks/{id}`: Delete a task

### Lists

- `GET /lists`: Retrieve a list of lists
- `GET /lists/{id}`: Retrieve a specific list
- `POST /lists`: Create a new list
- `PUT /lists/{id}`: Update an existing list
- `DELETE /lists/{id}`: Delete a list

## Schema

### Task

- `id` (integer, unique): The ID of the task
- `title` (string): The title of the task
- `description` (string): A description of the task
- `completed` (boolean): Whether the task has been completed
- `list_id` (integer): The ID of the list that the task belongs to

### List

- `id` (integer, unique): The ID of the list
- `name` (string): The name of the list

## Examples

### Retrieve a list of tasks

curl -X GET /tasks

HTTP/1.1 200 OK
[
{
"id": 1,
"title": "Grocery shopping",
"description": "Buy milk, bread, and eggs",
"completed": false,
"list_id": 1
},
{
"id": 2,
"title": "Laundry",
"description": "Wash and fold clothes",
"completed": true,
"list_id": 1
}
]


### Create a new task

curl -X POST /tasks -d '{ "title": "Take out trash", "description": "Empty trash cans", "completed": false, "list_id": 1 }'

HTTP/1.1 201 Created
{
"id": 3,
"title": "Take out trash",
"description": "Empty trash cans",
"completed": false,
"list_id": 1
}



## Requirements

- 
- MongoDB v4 or newer

## Running the API

1. Install dependencies: 
2. Start the API: 

## Testing the API

To run the test suite, use the following command:

