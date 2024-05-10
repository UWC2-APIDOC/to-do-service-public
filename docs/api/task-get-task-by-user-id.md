---
layout: page
---

# Get task by user ID

Returns all task objects that are associated with a specific `user_id` parameter, if any exist.

## URL

```shell

{server_url}/tasks/{user_id}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `user_id` | number | The ID of the user resource to which this task is assigned |

## Request headers

None

## Request body

None

## Return body

```json

{
    "user_id": 1,
    "title": "Grocery shopping",
    "description": "eggs, bacon, gummy bears",
    "due_date": "2024-02-20T17:00",
    "warning": "-10",
    "id": 1
},
{
    "user_id": 1,
    "title": "Chores list",
    "description": "sweep, dust, mop, vacuum",
    "due_date": "2024-02-20T17:00",
    "warning": "-10",
    "id": 2
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
