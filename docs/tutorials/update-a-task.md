# Tutorial: Update a task

Learn how to update an existing `task` for a `user` of the to-do service.

## Before you start

1. Make sure you’ve completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you’ll use for the tutorial.

2. Retrieve the `id` of the `task` you’d like to update. You can do this by sending a `GET` request to view all the existing tasks in the service.

3. Ensure that your local service is running. If it’s not, start it by running the below command in your command line (replacing <your-github-workspace> with your local clone of the repository).

    ```shell
    cd <your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```


## Update a task

Updating a `task` in the service requires that you send a `PUT` request to the server with the amended details of an existing `user` resource.

To update a task:

1. Open the Postman app on your desktop.

2. Set your base url to `http://localhost:3000`.

3. Create a new request with these values:
    * **METHOD**: PUT
    * **URL**: `{{http://localhost:3000}}/tasks/id`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
		
```js
		{
		    "user_id": 2,
		    "title": "Oil change for Honda",
		    "description": "20K auto service",
		    "due_date": "2025-03-10T09:00",
		    "warning": "-60",
		    "id": "3"
		}
```		

	You can change the value of any property in the request body. In the example above, the title, description, and due date have been changed.



 4. Click **Send** to make the request.

   In the response body that comes up, the task details should match the ones in your request body. Note that the example below displays the task’s updated title, description, and due date.

```js
{
    "user_id": 2,
    "title": "Oil change for Honda",
    "description": "20K auto service",
    "due_date": "2025-03-10T09:00",
    "warning": "-60",
    "id": "3"
}
```

You have now updated a task within the to-do service.

If you’d like to repeat this request in your favorite programming language, adapt the values from
the tutorial to the properties and arguments that the language uses to make REST API calls.

## Related topics

* [Add a new task](./add-a-new-task.md)
* [Delete a task](./delete-a-task.md)
* [Get tasks by title](../api/tasks-get-tasks-by-title.md)
* [Handling errors](../api/handling-errors.md)
