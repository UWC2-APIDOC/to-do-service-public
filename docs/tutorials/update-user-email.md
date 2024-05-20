---
layout: page
---

# Tutorial: Update a user's email

In this tutorial, you'll learn the operations to call to update a user's email.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you'll use for the tutorial.

## Update a user's email

You can update an existing user's email in the To-Do service. To do so, `PUT` an [`email`](../api/user/id/email) resource containing the user's details.

To update a user's email:

1. If your local service is not running, start it.

    ```shell
    cd <your-github-workspace>/to-do-service/api
    # Run the service and monitor its database file for updates
    json-server -w to-do-db-source.json
    ```

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request with these values:
    * **METHOD**: PUT
    * **URL**: `{{base_url}}/user/id/email`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        You can change the values of each property as you'd like.

        ```js
        {
            "email": "jen.jones@example.com"
        }
        ```

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this. Note that the email should be the same as you used in your **Request body** and the response should include the new user's `email`.

    ```js
    {
        "last_name": "Jones",
        "first_name": "Jenny",
        "email": "jen.jones@example.com",
        "id": 5
    }
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
