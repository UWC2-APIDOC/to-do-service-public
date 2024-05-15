---
layout: page
---

# Tasks category

Returns an array of  [`task`](task) objects that contains tasks that have the specified `category` parameter, if it exists.

## URL

```shell

{server_url}/tasks/{category}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `category` | string | The user-defined task category.  |

## Request headers

None

## Request body

None

## Return body

```js
{
    "user_id": 1,
    "title": "Grocery shopping",
    "description": "eggs, bacon, gummy bears",
    "due_date": "2024-02-20T17:00",
    "warning": "-10",
    "category": "shopping",
    "id": 1
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
