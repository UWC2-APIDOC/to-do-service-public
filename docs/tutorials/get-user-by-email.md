# Tutorial: Get a user by email

In this tutorial, you will learn how to get a user from the To-Do service by their email address.

Expect this tutorial to take about 15 minutes to complete.

## Before You start

Make sure you've completed the [Before you start a tutorial](../tutorials/before-you-start-a-tutorial.md)  topic on the development system you'll use for the tutorial.

This tutorial assumes you have set the `base_url` variable in Postman to `http://localhost:3000`. If you are not using variables in Postman, replace all occurrences of \{\{base_url\}\} in these examples with `http://localhost:3000`. For more information on using environments and variables in Postman, see [Using Variables inside Postman](https://blog.postman.com/using-variables-inside-postman-and-collection-runner/).

## Get a user by email

You can get a user by their email address by making a `GET` request to the user resource in the To-Do service.

Follow these steps to get a user by email:

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
5. To search by a specific email, in the URL field:
    1. Enter the base URL for the To-Do service, followed by the endpoint `/users`. 
    2. After the endpoint, type a question mark (`?`), followed by the `email` query parameter, the equals sign (`=`), and the desired email address.
    
The following is an example of such a URL:

<!-- {% raw %} -->
```
   {{base_url}}/users?email=<email address>
```
<!-- {% endraw %}) -->
* **Example Request:**
<!-- {% raw %} -->
```
     {{base_url}}/users?email=j.smith@example.com
```
<!-- {% endraw %}) -->
* **Example Response:**

     Watch the response body, which should look something like this.

     ```json
     [
         {
              "last_name": "Smith",
              "first_name": "John",
              "email": "j.smith@example.com",
              "id": "1"
         }
     ]
     ```

     **Note:** If no user matches the search criteria, the service will return an empty array (`[]`), indicating that there are no users with the specified email address.

     This completes the tutorial of getting a user by their email address. 
     
## Next steps

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.