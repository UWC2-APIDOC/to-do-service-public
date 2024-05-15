---
layout: page
---
# `user` resource

Base endpoint:

```shell
{server_url}/users
```

Contains information about the users of the service.

To have a task in the service, the user must be added to the service first.

## Resource properties

Sample `user` resource

```js
{
    "last_name": "Smith",
    "first_name": "Ferdinand",
    "email": "f.smith@example.com",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `last_name` | string | The user's last name |
| `first_name` | string | The user's first name |
| `email` | string | The user's email address |
| `id` | number | The user's unique record ID |

## Operations

The `user` resource supports these operations.

### READ (GET)

* [Get all users](users-get-all-users)
* [Get users by ID](users-get-user-by-id)
* [Get users by Email](users-get-user-by-email)
* [Get users by first names](users-get-users-first-names)

### CREATE (POST)

* [Create user](users-create-user)

### UPDATE (PUT/PATCH)

* [Update user by ID](users-update-by-id)
* [Change user email](users-change-user-email.md)
* [Change user property](users-change-user-property)

### DELETE

* [Delete users by email](users-delete-user-by-email)
* [Delete user by ID](users-delete-user-by-id)
