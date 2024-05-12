---
layout: page
---

# Tutorial: Update a user property 

Learn the operations to update one or more properties in a user record.

Expect this tutorial to take about 10 minutes to complete.

You can update any (or all) of these parameters: last name, first name, and email. In this demonstration, you learn how to update an existing user's email address.

## Before you start

Make sure you've completed the [Before you start a tutorial](before-you-start-a-tutorial) topic on the development system you'll use for the tutorial.

If your local service is not running, start it.

```
cd <your-github-workspace>/to-do-service/api
# Run the service and monitor its database file for updates
json-server -w to-do-db-source.json
```

When the service is running, start the Postman app on your desktop. Run a GET request `{server_url}/users/{id}` to locate the user's record and confirm their ID. You'll need the correct user ID to run a PATCH request and update a property.

## Update a property

To update a user record in the To-Do service, `Patch` a new [`user`](../api/user) resource containing the user's new details.

1. Go to the Postman app.
1. Create a new request with these values:
    * **METHOD**: PATCH
    * **URL**: `{server_url}/users/{id}`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        You can change the values of any property. In this example, we update the email address.

        ```js
        {
            "email": "jen.jones2@example.com"
        }
        ```

1. In the Postman app, click **Send** to make the request.
1. Watch for the response body, which should look something like this. In this example, the email address is new but the other parameters are unchanged.

    ```
    {
        "last_name": "Jones",
        "first_name": "Jenny",
        "email": "jen.jones2@example.com",
        "id": 5
    }
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.

Here is an example with cURL.

```
curl --location --request PUT 'localhost:3000/users/' \
--header 'Content-Type: application/json' \
--data-raw '        "email": "jen.jones2@example.com"'
```
