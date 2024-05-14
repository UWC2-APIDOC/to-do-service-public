---
layout: page
---

# Delete a task by ID

Deletes a [task](task.md) resource specified by the `id` parameter, if it exists.

## HTTP Method

DELETE

## URL

```shell
{server_url}/tasks/{id}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The ID of a task that you want to delete. |

## Request headers

None

## Request body

None

## Return body

None

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Resource deleted successfully |
| 404 | Error | Specified task  not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

For detailed information on errors, see section [Handling Errors in the To-Do Service API](handling-errors.md)
