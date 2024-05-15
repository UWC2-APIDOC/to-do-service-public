---
layout: page
---

# Get task by title

Returns an array of [`task`](task) objects with the specified `title` parameter, if any exist.



## URL

```shell

{GET} {server_url}/tasks?title={title}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `title` | String | The title or short description of the task | 

## Request headers

This request does not use any authorization. The endpoint is available to all tasks and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data to be posted. | Optional | application/json. Default value.  |
| Accept | The format of the data to be returned. | Optional | application/json. Default value. |


## Request body

In the request body, specify a JSON representation of the [`task`](task) object. The following table lists the properties that are required when you get a task. 

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | Number | The ID of the user resource to which this task is assigned |
| `title` | String | The title or short description of the task |
| `description` | String | The long description of the task|
| `due_date` | String | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the task is due |
| `warning` | Number | The number of minutes relative to the `due_date` to alert the user of the task. This is normally a negative number to alert the user before the `due_date`.|
| `id` | Number | The task's unique record ID |

## Return body

The following example shows the response. 

```js
[
    {
        "user_id": 15,
        "title": "Meet with trainer"
        "description:" "Intro session for exercise plan"
        "due_date": "2024-05-13T14:00",
        "warning": "-70"
        
    }
]
```

```js
[
    {
        "user_id": 16,
        "title": "Buy stamps at USPS"
        "description:" "Two sheets of forever stamps"
        "due_date": "2024-05-12T14:00",
        "warning": "-70"
        
    }
]
```
## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified task record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |