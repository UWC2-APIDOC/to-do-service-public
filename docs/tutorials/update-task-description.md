---
layout: page
---

# Update a task description

In this tutorial, you will learn how to use Postman to update a task description. This use case is common, since your users will need to to add task details as their deadlines approach. 

This tutorial takes about 15 minutes to complete. 

## Before you begin

Before starting this tutorial, install Postman and json-server. Then, sync the To-Do service to your  GitHub repository so that you can clone it to your desktop. For a complete set of steps, see [Before you start a tutorial](/docs/tutorials/before-you-start-a-tutorial.md). 

> ⚠️ The steps to run json-server are designed for Mac users, but you can easily adapt them to Windows or Linux. For example, on Windows, replace `json-server.sh` with `json-server.bat` from the source repository.

## Get a list of tasks

Unless you know the `id` of the task to update, start with listing all tasks in the To-Do service's database. 

##### To get a list of tasks:

1. In Terminal, start json-service. 

    ```shell
    cd path/to/<your-github-workspace>/to-do-service/api
    # Run the service against the database file
    ./json-server.sh -w to-do-db-source.json
    ```

2. In Postman, add a new request with these values:
   
    * **METHOD** — `GET`
    * **URL** — `http://localhost:3000/tasks`
    * **Headers** — `Content-Type: application/json`
    * **Request body** — None

3. In Postman, click **Send**.
   The To-Do service returns a JSON object that contains all tasks. Each task has the following format. Note the `id` of the task to update. 

    ```json
    {
        "user_id": 1,
        "title": "Grocery shopping",
        "description": "eggs, bacon, gummy bears",
        "due_date": "2024-02-20T17:00",
        "warning": "-10",
        "id": 1
    }
    ```

## Update the task description

Now that you know the task `id`, send a `PATCH` request to the `/tasks/{id}` endpoint to update the description. 

##### To update the task description:

1. If json-service is not running, start it in Terminal.

    ```shell
        cd path/to/<your-github-workspace>/to-do-service/api
        # Run the service against the database file
        ./json-server.sh -w to-do-db-source.json
    ```

2. In Postman, add a new request with these values:
    * **METHOD** — `PATCH`
    * **URL** — `http://localhost:3000/tasks/{id}`
    * **Headers** — `Content-Type: application/json`
    
3. In the **Request Body**, add only the updated `task_description`.

    ```json
    {
    "task_description": "Updated task description"
    }
    ```

4. Click **Send**. 
   The To-Do service updates the task description and returns a `200 OK` along with the updated task as a JSON object.  

## Next Steps

Now that you have verified this API workflow in Postman, you're ready to integrate it into your application. For more information, contact your customer success manager. 

## Related Topics

* [Task resource](docs/api/task.md)
* [Handing errors](docs/api/handling-errors.md)