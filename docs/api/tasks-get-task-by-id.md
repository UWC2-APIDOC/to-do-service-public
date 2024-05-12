---
layout: page
---

# Get task by ID

Returns an array of  [`task`](task) objects that contains only the task specified by the `id` parameter, if it exists.

## URL

```shell

{server_url}/task/{id}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record ID of the task to return |

## Request headers

None

## Request body

None

## Return body
| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | Number | The ID of the user resource to which this task is assigned |
| `title` | String | The title or short description of the task |
| `description` | String | The long description of the task|
| `due_date` | String | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the task is due |
| `warning` | Number | The number of minutes relative to the `due_date` to alert the user of the task. This is normally a negative number to alert the user before the `due_date`.|
| `id` | Number | The task's unique record ID |

Sample task response

```js
[
    {
        "user_id": 1,
        "title": "Grocery shopping",
        "description": "eggs, bacon, gummy bears",
        "due_date": "2024-02-20T17:00",
        "warning": "-10",
        "id": "1"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found | [comment: I cannot get the service to return a 404 error]
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |