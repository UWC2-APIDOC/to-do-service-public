---
layout: page
---

# Tutorial: Delete a task

In this tutorial, you will learn the operations to call to delete a task for a user of the service.

Expect this tutorial to take about 5 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you'll use for the tutorial.

## Delete a task

Deleting a task from the service requires that you send a `DELETE` request to the service with the `id` of the [`task`](../api/task) resource you want to remove.

To delete a task:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    - **METHOD**: DELETE
    - **URL**: `{{base_url}}/tasks/5` (replace `5` with the ID of the task you want to delete)
    - **Headers**:
        - `Content-Type: application/json`
4. Choose **Send** to make the request.
5. Watch for the response body, which should be empty, indicating that the task with the specified ID has been successfully deleted.

After completing this tutorial in Postman, you might want to repeat it in your favorite programming language. To do this, adapt the values from the tutorial to the properties and arguments that the language uses to make REST API calls.