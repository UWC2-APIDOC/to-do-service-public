---
layout: page
---

# First-Use: Enroll a new user

In this tutorial, you will enroll a new user, Jack, in the To-Do service so he can be assigned one of the existing tasks.

Expect this tutorial to take about 15 minutes to complete.

## Enroll a new user

You will enroll Jack using Postman, a user-friendly API client. Postman will allow you to easily `POST` a new [`user`](api/user) resource containing the user's details.

To enroll a new user:

1. First confirm our local service is running in the command window with the following:

    ```shell
    cd <your-github-workspace>/to-do-service/api
    # Run the service and monitor its database file for updates
    json-server -w to-do-db-source.json
    ```

1. Next, open the Postman app on your desktop.
1. In the Postman app, create a new request and input these values:
    * **METHOD**: POST
    * **URL**: `{{base_url}}/users`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        The following table lists the required properties for each user:

        | Property | Description | Type | Required | Notes |
        | -------------- | ------ | ------------ |------------ |------------ |
        | last_name | The user's last name. | string | Required |   |
        | first_name | The user's first name. | string | Required |  |
        | email | The user's email. | string | Required | A unique email is required. |

        In the Request Body, the JSON script of those properties will be entered like this:

        ```js
        {
            "last_name": "Wilson",
            "first_name": "Jack",
            "email": "jack.wilson@example.com"
        }
        ```

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this. Note that the names should be the same as you used in your **Request body** and the response should include the new user's `id`.

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
