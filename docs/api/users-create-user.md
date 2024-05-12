---
layout: page
---

# Create user

Creates a [`user`](user) who is registering with the to-do service.
The request body contains the new user details. 
You must specify the required properties for the user. 

## URL

```shell

{POST}{server_url}/users/
```

## Request headers

This request does not use any authorization. The endpoint is available to all users and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data to be posted. | Optional | application/json. Default value.  |
| Accept | The format of the data to be returned. | Optional | application/json. Default value. |

## Request body

In the request body, specify a JSON representation of the [`user`](user) object. The following table lists the properties that are required when you create a user. 

| Property | Description | Type | Required | Notes |
| -------------- | ------ | ------------ |------------ |------------ |
| last_name | The user's last name. | string | Required |   |
| first_name | The user's first name. | string | Required |  |
| email | The user's email. | string | Required | A unique email is required. |


## Sample request

The POST body should look something like this. You can change the values of each property as you’d like.

```js
[
    {
        "last_name": "Coughlan",
        "first_name": "Sinead",
        "email": "scough2@uw.edu",
    }
]
```

## Return body
The following example shows the response. Note that the names should be the same as you used in your **Request body** and the response should include the new user’s id. The user’s id is automatically generated when the user is created.

```js
[
    {
        "id": "f0d3",
        "last_name": "Coughlan",
        "first_name": "Sinead",
        "email": "scough2@uw.edu"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 201 | Created | User data created successfully. |
| 500 | Internal server Error | Invalid JSON. |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

