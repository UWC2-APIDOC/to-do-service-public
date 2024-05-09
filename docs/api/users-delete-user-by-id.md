# Delete user by ID

Removes the user you identify in the `id` parameter from the user resource, if the user exists.

## URL

```shell

{server_url}/users/{id}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record ID of the user to delete |

## Request headers

Content-Type: application/json

## Request body

DELETE {server_url}/users/{id}

## Return body
Returns the user you deleted from the user resource

```js
[
    {
        "last_name": "Jones",
        "first_name": "Jill",
        "email": "j.jones@example.com",
        "id": "2"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Action completed successfully |
| 202 | Accepted| Action has been queued |
| 204 | No Content| Action has been performed, but the response does not include an entity |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Related topics
[Enroll a new user](../tutorials/enroll-a-new-user)

