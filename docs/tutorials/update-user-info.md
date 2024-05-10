# Tutorial: Update a specific user's information

In this tutorial, you will learn how to change an existing user's information.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you have completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you will use for this tutorial.

## Find an existing user's ID

Unless you already know the user's unique ID, you must first retrieve a list of the available users. To do this, use the GET method for {base_url}/users. If you already know the user's ID, skip this step.

View a list of all your users

1. If your local service is not running, start it.

    ```shell
    cd <your-github-workspace>/to-do-service/api
    # Run the service and monitor its database file for updates
    json-server -w to-do-db-source.json
    ```

1. On your desktop, open the Postman app.
1. In the Postman app, create a new request with the values below.
    * **METHOD**: GET
    * **URL**: `{base_url}/users`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
       None

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look similar to the text below. Make note of the `id` for the user (or users) you want to change.

  
```js
[
    {
        "last_name": "Smith",
        "first_name": "Ferdinand",
        "email": "f.smith@example.com",
        "id": "1"
    },
    {
        "last_name": "Jones",
        "first_name": "Jill",
        "email": "j.jones@example.com",
        "id": "2"
    },
    {
        "last_name": "Martinez",
        "first_name": "Marty",
        "email": "m.martinez@example.com",
        "id": "3"
    },
    {
        "last_name": "Bailey",
        "first_name": "Bill",
        "email": "b.bailey@example.com",
        "id": "4"
    }
]
```
## Update an existing user's information

To update information in an existing user's account, do the following:

1. If your local service is not running, start it.

    ```shell
    cd <your-github-workspace>/to-do-service/api
    # Run the service and monitor its database file for updates
    json-server -w to-do-db-source.json
    ```

1. On your desktop, open the Postman app. In this example, you will change the `first_name` of user 3 from "Marty" to "Maria".
1. In the Postman app, create a new request with the values below.
    * **METHOD**: PUT
    * **URL**: `{base_url}/users/3`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
      
    ```js
       {
        "last_name": "Martinez",
        "first_name": "Maria",
        "email": "m.martinez@example.com",
        "id": "3"
       }
    ```

1. In the Postman app, choose **Send** to make the request.
1. Congratulations! The response body should show the updated `first_name` property for user 3, as in the output below.

```js
  [
   
    {
        "last_name": "Martinez",
        "first_name": "Maria",
        "email": "m.martinez@example.com",
        "id": "3"
        
    }
    
  ]
```

## Next steps
After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
