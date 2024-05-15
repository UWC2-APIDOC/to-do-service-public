---
layout: page
---

# Tutorial: Delete a task

In this tutorial, you learn the operations to call to
delete a task for a user of the service.

## Before you start

Make sure you've completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you'll use for the tutorial.

## Delete a task

Deleting a task from the service requires that you remove (`DELETE`) an existing [`task`](../api/task) resource to the service.

To delete a task:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request with these values:
    * **METHOD**: DELETE
    * **URL**: `{{base_url}}/tasks/{id}`

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this. Note that the response should include only the user's `id` targeted for deletion.

    ```js
    {
        "user_id": 3,
        "title": "Get new tires",
        "description": "Get new tires for Hoppity",
        "due_date": "2024-03-11T14:00",
        "warning": "-60",
        "id": 5
    }
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
