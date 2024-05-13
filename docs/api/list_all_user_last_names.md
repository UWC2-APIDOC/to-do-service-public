---
layout: page
---

# List all user last names

This page goes over how to list all user last names that are registered on the to-do service.

## Base Endpoint: 

GET /users/last_names

This endpoint retrieves the last names of all users.

### Properties:

  * ' last_names ': Is an array that contains the last names of all users. Specificially an array of strings representing the last names of users.

### Operations: 

  * ' GET /users/last_names ': Retrieves the last names of all users.

#### Examples: 

Request:

curl -X GET https://api.example.com/users/last_names

Response:

{
  "last_names": [
    "Doe",
    "Smith",
    "Johnson"
  ]
}

| Property Name | Type   | Description                           |
|---------------|--------|---------------------------------------|
| last_names    | Array  | An array containing user last names.  |

#### Additional Links:

[Get all users](users-get-all-users.md)
