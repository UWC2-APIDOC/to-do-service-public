---
layout: page
---


# Find tasks by user ID

In this tutorial, you learn the operations to call to find tasks by auto-generated user ID.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

1. Make sure you've completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you'll use for the tutorial.
1. Check whether the `{base_url}` in Postman collection points to `http://localhost:3000`. If not set correctly, you will see local host errors. For assistance setting up the variables for your import collection, refer to [set environment variables in Postman](https://learning.postman.com/docs/sending-requests/variables/environment-variables/).  

## About this task

You can retrieve a task or multiple tasks by a specific user ID.

Steps to find tasks by user ID:

1. Open your Postman desktop application. 
1. Go to the **To-Do-mock** service test json  collection containing the list of users and tasks associated with each user. 
1. Expand the **tasks** folder.
1. Expand the **tasks:READ** method.
1. From the list, select *Get tasks by user_id* and click on the three dots.
1. From the options, select **Duplicate** and make a copy of the *Get tasks by user_id* request.
1. (**Optional**) Make sure to select the **GET** method type. 
1. (**Optional**) Rename the request. Here's an example: **Get tasks by user_id_2**. 
1. Save the new request.
1. Specify an user ID to the base URL request. For example: `http://localhost:3000/tasks?user_id=1`. Alternatively, you can modify the **Query Params** tab and then add a user ID.  

        | Property  | Type | Description|
        | User_id  | Number|**Required** Indicates a numeric value associated with each task a specific user owns.|
1. Click **Send** to initiate your new request.

## Sample response

Here's an example response with all the tasks associated with user id = 1:

```js
[
    {
        "user_id": 1,
        "title": "Grocery shopping",
        "description": "eggs, bacon, gummy bears",
        "due_date": "2024-02-20T17:00",
        "warning": "-10",
        "id": "1"
    },
    {
        "user_id": 1,
        "title": "Piano recital",
        "description": "Daughter's first concert appearance",
        "due_date": "2024-04-02T15:00",
        "warning": "-30",
        "id": "2"
    }
]
```
## Troubleshooting tips

- [Error handling](../api/handling-errors.md)
- [Properties cheat sheet for successful requests](../api/cs-for-successful-requests.md)


## Next steps

1. Integrate this service in your workflow for further downstream analysis.  
1. Create an automated workflow between tasks and users using this service and a set of services included in the collection.

