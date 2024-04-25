# Tutorial: Get tasks by a property
Get a list of tasks that match a property.

## Before you start
1. Set up the To-Do service on your system. See [Before you start a tutorial](/docs/tutorials/before-you-start-a-tutorial.md).

2. Start the To-Do service on your local computer.

## Get tasks by a property

1. Open the Postman app on your desktop.

2. Create a `GET` request.

    ```
    {base_url}/tasks?{property}={value}
    ```
    See [Task properties](//docs/api/get-task-ref.md).
    
    >**NOTE**: The value must be an exact match to return a valid response.

3. Click **Send**.
4. You'll receive a response with matching tasks.

## Example

### Request

```
{base_url}/tasks?due_date=2024-04-02T15:00
```
### Response

```
[
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

## Next steps

[Add a new task](/docs/tutorials/add-a-new-task.md)
[Delete a task](/docs/tutorials/delete-a-task.md)