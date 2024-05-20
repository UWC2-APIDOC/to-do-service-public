---
layout: page
---

# Tutorial: Delete tasks by due date

In this tutorial, you will learn the operations to delete all tasks older than a specified date.

This tutorial requires two steps:

1. Use the `GET` request to retrieve the tasks whose `due_date` parameter is later than a specified date.
2. Delete the tasks retrieved in step 1 using the `DELETE` request.

Expect this tutorial to take about 15 minutes to complete.

## Prerequisites

Before you start this tutorial:

1. Make sure you've completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you'll use for the tutorial.
2. Make sure your local service is running. If it's not, start it with this command:

    ```shell
    cd <your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```

3. Open the Postman app.

## Step 1: Get tasks older than a specified date

To get a list of tasks older than specified date, you must send a `GET` request to the service with a parameter of `due_date_lt`. To do so, follow these steps:

1. In the Postman app, create a new request with these values:

    - **METHOD**: GET
    - **URL**:

    ```text
    {{base_url}}/tasks?due_date_lt={date}
    ```

    (replace `{date}` with the date you want to use a reference. The date must be in the following date format: `YYYY-MM-DDTHH:mm`)
    - **Headers**:
        - `Content-Type: application/json`

2. Select **Send** to make the request.
3. Watch for the response body, which should contain the list of tasks with the `due_date` later than the date you specified.

## Step 2: Delete tasks

To delete the tasks you retrieved in step 1, follow these steps for every single task returned in the previous request:

1. In the Postman app, create a new request with these values:
    - **METHOD**: DELETE
    - **URL**: `{{base_url}}/tasks/{id}` (replace `{id}` with the ID of the task you want to delete)
    - **Headers**:
        - `Content-Type: application/json`
2. Select **Send** to make the request.
3. Watch for the status code, which should be `200`. This indicates that the task with the specified ID has been successfully deleted.

After completing this tutorial in Postman, you might want to repeat it in your favorite programming language. To do this, adapt the values from the tutorial to the properties and arguments that the language uses to make REST API calls.
