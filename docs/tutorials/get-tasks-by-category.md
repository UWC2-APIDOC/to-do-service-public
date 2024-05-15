---
layout: page
---

# Tutorial: Get tasks by category

You will learn how to retrieve tasks by category.  
⏱️ Estimated time: 5 minutes

## Before you start

* Set up your development environment: [Before you start a tutorial](before-you-start-a-tutorial)
* Prepare sample data: Create at least one user, at least one task, and at least one category
* Start your server:  
    Example command: 
        ```shell
        cd <your-github-workspace>/to-do-service/api
        json-server -w to-do-db-source.json
        ```

## Retrieving tasks with a specific category

Retrieving tasks that have a specific category requires sending a `GET` request to the appropriate endpoint with the task category string.

To retrieve tasks with a specific category:

1. In the Postman app, create a new request with the following values:
    - **METHOD**: GET
    - **URL**: `{base_url}/tasks?category=<category_name>`
        Replace `<category_name>` with the category name for the tasks you want to retrieve.
    - **Headers**:
        - `Content-Type: application/json`

2. Click  **Send** to make the request.
3. Review the response body, which should contain an array of task objects that have your specified `category` property value. 

Example response body:  

    ```json
    [
        {
        "user_id": 1,
        "title": "Grocery shopping",
        "description": "eggs, bacon, gummy bears",
        "due_date": "2024-02-20T17:00",
        "warning": "-10",
        "category":"errand_personal",
        "id": "1"
        },

        {
        "user_id": 2,
        "title": "Oil change",
        "description": "5K auto service",
        "due_date": "2024-03-10T09:00",
        "warning": "-60",
        "category":"errand_personal",
        "id": "3"
        }
    ]
    ```

## Next steps
Try this tutorial in other programming languages by adapting these properties to the properties and arguments that your target language uses to make REST API calls.
