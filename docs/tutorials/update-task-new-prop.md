# Tutorial: Add a new property to an existing task

In this tutorial, you will learn how to update an existing task with a new property.

Let’s suppose, for example, that a car *oil change* is a high priority to-do task.
You decide to add **priority** as a new task property.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you have completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you will use for this tutorial.

If your local service is not running, start it.

    ```shell
    cd <your-github-workspace>/to-do-service/api
    # Run the service and monitor its database file for updates
    json-server -w to-do-db-source.json
    ```


## About the task

There's two parts to this task.

1. Retrieve the task to update.
2. Add a new property to the selected task.

## Retrieve the task to update

To view all tasks, make a `GET` call to the [`task`](../api/task) resource.

1. On your desktop, open the Postman app.
1. To create a new request, click **New** > **HTTP**. Give the request a title.
1. Specify these request values in the right-frame window:

    | UI Element | Values | Required | Notes |
    | -------------- | ------ | ------------ |------------ |
    | **METHOD** | GET | Required | Locate the drop-down menu next to the URL field. |
    | **URL** | `{base_url}/tasks` <br /> or`{base_url}/tasks/{id}`  | Required | The **base_url** variable is typically set to `http://localhost:3000`. Specify {id} to return a specific task. Otherwise all tasks are returned. |
    |**params** | `Key/Value` | Optional |  You can specify task attributes as key/value query parameters. For example: *title/Oil change*. Note that task titles are case sensitive.  |
    |**Headers** | `Content-Type` | Optional | The format of the data to be posted. Default value is application/json. |
    |**Request body** | None |  |  |

1. Click **Send** to make the request.
1. Review the response body and verify the task {id} you want to update. The complete or refined task list looks something like this.

    ```js
        [
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

## Add a new property to a selected task

To update a selected task, make a `PUT` call to the [`task`](../api/task) object containing the {id}.
Assuming you know the task {id}, proceed as follows:

1. On your desktop, open the Postman app.
1. To create a new request, click **New** > **HTTP**. Give the request a title.
1. Specify these values in the right-frame window:

    | UI Element | Values | Required | Notes |
    | -------------- | ------ | ------------ |------------ |
    | **METHOD** | PUT | Required | Locate the drop-down menu next to the URL field. |
    | **URL** | `{base_url}/tasks/{id}` | Required | The **base_url** variable is typically set to `http://localhost:3000`. Specify the {id} of the selected task returned in your `GET` call. |
    |**Headers** | `Content-Type` | Optional | The format of the data to be posted. Default value is application/json. |
    |**Request body** | The selected task details. | Required  | You can copy/paste the JSON response body returned in your `GET` call. |

1. To add a new property, for example, *priority*, insert the content on a new line in the request body like this.

    ```js
        [
            {
                "user_id": 2,
                "title": "Oil change",
                "description": "5K auto service",
                "due_date": "2024-03-10T09:00",
                "priority": "High",
                "warning": "-60",
                "id": "3"
            }
        ]
    ```
1. Click **Send** to make the request.
1. Review the response body and verify the inclusion of the updated property. You should see a 200 OK status code that indicates success.

## Next steps
To further validate the `PUT` request, run the `GET` call again. The task returned should reflect the new property in the response body.

## Related information

* [Handling errors](../api/handling-errors.md)
