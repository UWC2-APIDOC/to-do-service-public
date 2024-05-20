---
layout: page
---

# Tutorial: Get tasks by title

In this tutorial, you learn the operations to return a list of tasks with the same title.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you'll use for the tutorial.

## Get tasks by title

Returning a list of tasks from the service requires you to perform a get (`GET`) request on the [`task`](../api/task) resources in the service.

To get tasks by their title:

1. Make sure your local service is running. If it is not running, start it by using this command:

    ```shell
    cd <your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```

1. Open the Postman app on your desktop.
1. Create a new request with these values:
    * **METHOD**: GET
    * **URL**: `{{base_url}}/tasks?title=<replace this text with full title>`
   
   **Example:**

   `http://localhost:3000/tasks?title=Piano recital`
   
      **Note:** Title values are case sensitive.


1. In the Postman app, select **Send** to make the request.
1. Watch for the response body, which should look something like the following:

    ```js
   [
    {
        "user_id": 1,
        "title": "Piano recital",
        "description": "Daughter's first concert appearance",
        "due_date": "2024-04-02T15:00",
        "warning": "-30",
        "id": "2"
    },
    {
        "id": "eb1b",
        "title": "Piano recital",
        "description": "Piano recital for Jennifer",
        "due_date": "2024-05-11T15:00",
        "warning": "-75"
    }
   ]
    ```
  
  If there are no titles matching the entered search value, an empty array is returned.

After doing this tutorial in Postman, you might like to repeat it in your favorite programming language. To do this, adapt the values from the tutorial to the properties and arguments that the language uses to make REST API calls.
