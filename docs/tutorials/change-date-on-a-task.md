# Tutorial: Change the due date on a task

In this tutorial, you will learn how to change the due date on a task.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you have completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you will use for this tutorial.

## Find an existing task

Unless you already know the task's unique ID, you must first retrieve a list of tasks. To do this, use the GET method for {base_url}/tasks.

View a list of all tasks

1. If your local service is not running, start it.

    ```shell
    cd <your-github-workspace>/to-do-service/api
    # Run the service and monitor its database file for updates
    json-server -w to-do-db-source.json
    ```

1. On your desktop, open the Postman app.
1. In the Postman app, create a new request with the values below.
    * **METHOD**: GET
    * **URL**: `{base_url}/tasks`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
       None

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look similar to the text below. Make note of the `id` for the task (or tasks) you want to change.

```js
[
    {
        "task",
        "id": "1"
    },
    {
        "task",
        "id": "2"
    },
    {
        "task",
        "id": "3"
    },
    {
        "task",
        "id": "4"
    }
]
```

## Update an existing task's due date

To update the properties of an existing task resource, do the following:

1. If your local service is not running, start it.

    ```shell
    cd <your-github-workspace>/to-do-service/api
    # Run the service and monitor its database file for updates
    json-server -w to-do-db-source.json
    ```

1. On your desktop, open the Postman app. In this example, you will change the `due_date` of task 3 from "March 11" to "March 18".
1. In the Postman app, create a new request with the values below.
    * **METHOD**: PUT
    * **URL**: `{base_url}/tasks/3`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:

        ```js
        {
            "task",
            "id": "3"
        }
        ```

1. In the Postman app, choose **Send** to make the request.
1. Congratulations! The response body should show the updated `due_date` property for user 3, as in the output below.

```js
  [
   
    {
        "task,
        "id": "3"
        
    }
    
  ]
```

## Next steps

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
