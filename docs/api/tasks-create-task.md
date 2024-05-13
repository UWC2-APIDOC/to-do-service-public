---
layout: page
---

# Create a task

Creates a new [`task`](task) for a user of the to-do service.
The request body contains the new task details. 
You must specify the required properties for the new task. 

## URL

```shell

{POST}{server_url}/tasks/
```

## Request headers

This request does not use any authorization. The endpoint is available to all users and applications.

No headers required.

## Request body

In the request body, specify a JSON representation of the [`task`](task) object. The following table lists the properties that are required when you create a task. 

| Property | Description | Type | Required | Notes |
| -------------- | ------ | ------------ |------------ |------------ |
| title| The name of the task.| string | Required |   |
| description | A short description of the task. | string | Required |  |
| due-date | The due date of the task. | datetime | Required |  |


## Sample request

The POST body should look something like this. You can change the values of each property as you’d like.

```js
[
    {
        "title": "Assignment 7",
        "description": "Submit week 7 assignment",
        "due_date": "2024-05-14T23:59",
    }
]
```

## Return body
The following example shows the response. Note that the task title should be the same as you used in your **Request body** and the response should include the new task's id. The task's id is automatically generated when the task is created.

```js
[
    {
        "id": "4097",
        "title": "Week 7 assignment",
        "description": "Submit week 7 assignment",
        "due_date": "2024-05-14T23:59"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 201 | Created | Task data created successfully. |
| 500 | Internal server Error | Invalid JSON. |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |