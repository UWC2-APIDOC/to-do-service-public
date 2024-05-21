---
layout: page
---
# Make your first API call

This tutorial explains how to use the To-Do service API to get a list of all users. It also explains how to read the API response and troubleshoot errors. To make the request, you will use [Postman](https://www.postman.com/downloads/) to call a mock endpoint run by [json-server](https://www.npmjs.com/package/json-server).

Expect this tutorial to take about 15 minutes.

## Before you begin

Before you start, install Postman and json-server. Then, fork the [To-Do service](https://github.com/UWC2-APIDOC/to-do-service-public) to your own repository and clone it to your desktop. For step-by-step instructions, see [Before you start a tutorial](../tutorials/before-you-start-a-tutorial.md).

## Send the request

You need to get a list of users from the To-Do service before you can assign tasks or add new users, so it is a prerequisite for using the service further. To make the request, you will call the `/users` endpoint.

### To get a list of users

1. In your terminal emulator, start json-service.

    ```shell
    cd path/to/<your-github-workspace>/to-do-service/api
    # Run the service against the database file
    ./json-server.sh -w to-do-db-source.json
    ```

1. In Postman, add a new request with these values:

    * **METHOD** — `GET`
    * **URL** — `http://localhost:3000/users`
    * **Headers** — `Content-Type: application/json`
    * **Request body** — None

1. In Postman, click **Send**.
   The To-Do service returns a JSON array containing one object for each user.

    ```json
    {
    "last_name": "John",
    "first_name": "Doe",
    "email": "john.doe@example.com",
    "id": "1"
    }
    ```

In the response, `last_name`, `first_name`, `email`, and `id` indicate the user details. To learn more, see [user resource](user.md).

## Troubleshooting

For successful requests, the To-Do Service returns a `200 OK`, along with the user list in the response body. HTTP response status codes help you to diagnose any errors.

Common errors you may encounter when using this tutorial are:

* **404 Not Found** — Incorrect endpoint URL, potentially from a typo.
* **405 Method Not Allowed** — Inappropriate HTTP method, such as POST instead of GET.
* **ECONNREFUSED** — The json-server is not running or has stopped responding.

For a list of all errors supported by the To-Do service as well as troubleshooting suggestions, see [Handling Errors in the To-Do Service API](handling-errors.md).

## What to do next

Now that you have used the To-Do service to request a list of users, you can proceed with your integration or learn more about the service. The following topics provide next steps.

* [Enroll a new user](../tutorials/enroll-a-new-user.md)
* [Get tasks for a user](../tutorials/get-tasks-for-a-user.md)
* [Add a new task](../tutorials/add-a-new-task.md)
