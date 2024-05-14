---
layout: page
---


# Parameters for successful requests

This section highlights the required and optional parameters for the operations of the To-Do service.

To get a successful response from the following operations, you must specify at least the `required` properties listed under each task. 



## Add a new task
| Property| Type|Description|
|---|---|---|
|user_id | Number   |Indicates the user-specified numeric value associated with a new task.|
| title | String |Indicates a brief note about the task that you want to add.|
| description | String | Description of the task.   |
| due_date  | String (format: YYYY-MM-DD)   | Completion date of the task.   |
| warning  | String  | Indicates the user-specified note that can impact a task.|


## Find an existing user's id

| Property| Type|Description|
|---|---|---|
|last_name  |String| Last name of the user.|
|first_name |String|First name of the user.|
|email   |String| Email address   |
|id| Number  | Indicates the user-specified identifier associated with the user name.|


## Delete a task

| Property| Type|Description|
|---|---|---|
|  ID | Number | Indicates the id of the task you want to delete.|


## Find tasks by user ID


| Property| Type|Description|
|---|---|---|
| ID  | Number| Indicates the user-specified ID of the task you want to find.|



