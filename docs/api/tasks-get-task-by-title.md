---
layout: page
---

# Get tasks by title

Returns an array of  [`task`](task) objects that contain only the tasks specified by the `title` parameter, if they exist.

## URL

```shell

{server_url}/tasks?title=<replace this text with full title>
```

**Example:**

`http://localhost:3000/tasks?title=Piano recital`
   
**Note:** Title values are case sensitive.

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `title` | string | The record title of the task to return |

## Request headers

None

## Request body

None

## Return body

```js
  [
    {
        "user_id": 1,
        "title": "Piano recital",
        "description": "Daughter's first concert appearance",
        "due_date": "2024-04-02T15:00",
        "warning": "-30",
        "id": "2"
    },
    {
        "id": "eb1b",
        "title": "Piano recital",
        "description": "Piano recital for Jennifer",
        "due_date": "2024-05-11T15:00",
        "warning": "-75"
    }
 ]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified task record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |