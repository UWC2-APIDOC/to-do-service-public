---
layout: page
---

# Update user by ID

Allows the editing of [`user`](user) objects that already exist. You will need to know the `id` parameter of the user you want to edit.

> [!IMPORTANT]
> The request body replaces the current properties of the `user`.
> Properties that you don't want to change, must have their current values assigned in the request body,

## HTTP Method
PUT

## URL

```shell
{server_url}/users/{id}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record ID of the user to return |

## Request headers

| Key | Value |
|---|---|
| Content-Type | application/json |

## Request body parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `last_name` | string | The user's last name |
| `first_name` | string | The user's first name |
| `email` | string | The user's email address |
| `id` | number | This is not required and cannot be changed by this process |

## Example Request Body

```json
{
    "last_name": "Bailey",
    "first_name": "Bill",
    "email": "b.bailey@example.com"
}
```


## Return body

```js
[
    {
      "last_name": "Bailey",
      "first_name": "Bill",
      "email": "b.bailey@example.com",
      "id": "4"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
