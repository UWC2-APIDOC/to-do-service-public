---
layout: page
---

# Get task by due date

Returns an array of  [`task`](task) objects that contains only the task specified by the `due_date` parameter, if it exists.

## URL

```shell

{server_url}/tasks/{due_date}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `due_date` | string | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the task is due |

## Request headers

None

## Request body

None

## Return body

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
| 404 | Error | Specified task record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
