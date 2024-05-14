---
layout: page
---

# Tutorial: Get tasks for a user

In this tutorial, you will learn how to  retrieve tasks
associated with a specific user in the service.

Expect this tutorial to take about 10 minutes to complete.

## Before you start

Make sure you have completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you will use for the tutorial.

## Retrieve tasks for a specific user

Retrieving tasks for a specific user from the service requires sending a `GET` request to the appropriate endpoint with the user's ID.

To retrieve tasks for a specific user:

1. Ensure your local service is running. If not, start it by navigating to the API directory and running the JSON server with the following command:

    ```shell
    cd <your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```

1. Open the Postman app on your desktop.
1. Create a new request with the following values:
    - **METHOD**: GET
    - **URL**: `{base_url}/tasks?user_id=1`
        Replace `<user_id>` with the ID of the user whose tasks you want to retrieve.
    - **Headers**:
        - `Content-Type: application/json`

1. Click  **Send** to make the request.
1. Review the response body, which should contain an array of tasks associated with the specified user. Each task object should include details such as `title`, `description`, `due_date`, `warning`, `id`, etc.

    ```json
    [
        {
        "user_id": 1,
        "title": "Grocery shopping",
        "description": "eggs, bacon, gummy bears",
        "due_date": "2024-02-20T17:00",
        "warning": "-10",
        "id": "1"
        },

        {
        "user_id": 2,
        "title": "Oil change",
        "description": "5K auto service",
        "due_date": "2024-03-10T09:00",
        "warning": "-60",
        "id": "3"
        }
    ]
    ```

## Next steps
After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
