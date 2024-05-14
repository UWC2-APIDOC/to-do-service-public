---
layout: page
---


# Cheat sheet properties for successful requests

This section highlights the required and optional parameters for the operations of the To-Do service.

To get a successful response from the following operations, you must specify at least the `required` properties listed under each task. 



## Add a new task

- **HTTP method**: POST
- **URL**: `{{base_url}}/tasks`

| Property| Type|Description|
|---|---|---|
|user_id | Number   |Indicates the user-specified numeric value associated with a new task.|
| title | String |Indicates a brief note about the task that you want to add.|
| description | String | Description of the task.   |
| due_date  | String (format: YYYY-MM-DDTHH:MM:SS)   | Completion date of the task.   |
| warning  | number| When to remind the user of the task, relative to the `due_date`. Negative numbers indicate before the `due_date`, and positive numbers, after. |


## Find an existing user's id

- **HTTP method**: GET
- **URL**: `{{base_url}}/users/ID`

| Property| Type|Description|
|---|---|---|
|last_name  |String| Last name of the user.|
|first_name |String|First name of the user.|
|email   |String| Email address   |
|id| Number  | Indicates the user-specified identifier associated with the user name.|


## Delete a task

- **HTTP method**: DELETE
- **URL**: `{{base_url}}/task/ID`

| Property| Type|Description|
|---|---|---|
|  ID | Number | Indicates the id of the task you want to delete.|


## Find tasks by user ID

- **HTTP method**: GET
- **URL**: `{{base_url}}/tasks?user_id`


| Property| Type|Description|
|---|---|---|
| ID  | Number| Indicates the user-specified ID of the task you want to find.|



