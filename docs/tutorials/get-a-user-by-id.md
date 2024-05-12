# Tutorial: Get a user by ID

In this tutorial, you will learn how to get a user by their ID from the To-Do service.

Expect this tutorial to take about 15 minutes to complete.

## Before You Start

Make sure you've completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you'll use for the tutorial.

This tutorial assumes you have set the `base_url` variable in Postman to `http://localhost:3000`. 
If you are not using variables in Postman, replace all occurrences of \{\{base_url\}\} in these examples with `http://localhost:3000`. For more information on using environments and variables in Postman, see [Using Variables inside Postman](https://blog.postman.com/using-variables-inside-postman-and-collection-runner/).

## Get a user by ID

You can get a user by their ID by making a `GET` request to the user resource in the To-Do service.

Follow these steps to get a user by ID:

1. If your local service is not running, start it:

    ```shell
    cd <your-github-workspace>/to-do-service/api
    # Run the service and monitor its database file for updates
    json-server -w to-do-db-source.json
    ```
    
    * Replace `<your-github-workspace>` with the path to your To-Do service clone on your system.

2. Open the Postman app on your desktop.
3. Click the **New** button in Postman and select **HTTP** to create a new request.
4. Ensure **GET** is selected from the dropdown menu next to the request URL.
5. In the URL field, enter the base URL for the To-Do service followed by the endpoint `/users`, for example:
<!-- {% raw %} -->
```
    {{base_url}}/users
```
<!-- {% endraw %}) -->
   
6. To search for a specific ID, append a question mark (`?`) to `/id` in the URL, followed by the relevant query parameters, and then click **Send** to submit the `GET` request to the To-Do service.
  
      **Example Request:**      
<!-- {% raw %} -->
```
      {{base_url}}/users?lid=1
```
<!-- {% endraw %}) -->
      **Example Response:**
    
      ```json
      [
          {
              "last_name": "Doe",
              "first_name": "Jamie",
              "email": "jamie.doe@example.com",
              "id": "1"
          }
      ]
      ```
    
   

**Note:** If no user matches the search criteria, the service will return an empty array (`[]`), indicating that there are no users with the specified names.

