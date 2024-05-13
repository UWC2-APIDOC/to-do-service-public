---
layout: page
---

# Tutorial: Get a task by due date

In this tutorial, you learn the operations to call to
get a task by the due date.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you'll use for the tutorial.

## Get a task by due date

Finding a task by the due date requires that you retrieve (`GET`) the details of a [`task`](../api/task.md) using the `due_date` parameter.

To get a task by due date:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `{{base_url}}/tasks?due_date={due_date value}`
        **Note:** Make sure to use the [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format for the `due_date` value.
        
4. In the Postman app, choose **Send** to make the request.
5. Watch for the response body, which should look something like this. 

    ```js
    {
        "user_id": 1,
        "title": "Grocery shopping",
        "description": "eggs, bacon, gummy bears",
        "due_date": "2024-02-20T17:00",
        "warning": "-10",
        "id": "1"
    }
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
