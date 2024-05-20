---
layout: page
---

# Get user by  name

Returns an array of  [`user`](user) objects that contains only the user specified by the `first_name` parameter, if it exists.

## URL

```shell

{server_url}/users?first_name=<first name to find>
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `first_name` | string | The first name of the user to return |

## Request headers

None

## Request body

None

## Return body

```js
[
  {
        "last_name": "Smith",
        "first_name": "Ferdinand",
        "email": "f.smith@example.com",
        "id": 1
  }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified property not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
