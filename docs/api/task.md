---
layout: page
---
# `task` resource

Base endpoint

```shell
{server_url}/tasks
```

Contains information about tasks stored for the users of the service.

**This is a new line of text added for assignment 3!**

To have a task in the service, the user must be added to
the service first.

## Resource properties

Sample `task` resource

```js

{
    "user_id": 1,
    "title": "Grocery shopping",
    "description": "eggs, bacon, gummy bears",
    "due_date": "2024-02-20T17:00",
    "warning": "-10",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | Number | The ID of the user resource to which this task is assigned |
| `title` | String | The title or short description of the task |
| `description` | String | The long description of the task|
| `due_date` | String | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the task is due |
| `warning` | Number | The number of minutes relative to the `due_date` to alert the user of the task. This is normally a negative number to alert the user before the `due_date`.|
| `id` | Number | The task's unique record ID |

## Operations

The `task` resource supports these operations.

## READ (GET)

* [Get all tasks _(coming soon)_](#resource-properties)
* [Get task by ID](tasks-get-task-by-id.md)
* [Get task by user ID](task-get-task-by-user-id.md)
* [Get task by title](tasks-ref-topic-get-task-by-title)

## CREATE (POST)

* [Create a task](tasks-create-task.md/)

## UPDATE (PUT/PATCH)

* [Update a task with PATCH](update-task-with-patch.md)
