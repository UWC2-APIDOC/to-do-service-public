---
layout: page
---

# Update user properties

The Patch request updates the specified property but does not change the other parameters in the [`user`](user) object. 


**Note** : *After creating a user, a unique identifier (ID) is assigned. Provide the ID for the user in the REST URL.* 

## URL

```
{server_url}/users/{id}
```
## Method
PATCH


## Params
This table lists the properties that can be updated.   

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `email` | string | The user's new email address that will replace the address in the current record. |
| `last_name` | string | The user's new last name. |
| `first_name` | string | The user's new first name. |


## Request headers

None.

## Sample request body
This example updates the user's email address. The other parameters are not changed.

```
[
    {
        "email": "marty2@example.com",
    }
]
```

## Sample return body
This return shows the updated user record with a new email address.

```
[
    {
        "last_name": "Martinez",
        "first_name": "Marty",
        "email": "marty2@example.com",
        "id": "3"
    }
]
```


## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Removes the user and returns an empty response. |
| 404 | Error | Specified user record not found. |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |


## Request example

cURL 
```
curl --location --request PATCH 'localhost:3000/users/3' \
--header 'Content-Type: application/json' \
--data-raw '    {
        "email": "marty2@example.com"
    }'
``` 
