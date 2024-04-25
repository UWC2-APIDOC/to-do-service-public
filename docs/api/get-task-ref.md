# Reference:  Get tasks by a property
## URL
```
{base_url}/tasks?{property}={value}
```
Gets a list of tasks matching the specified property.

## Required parameters

| Parameter name | Type | Description |
| ---- | ---- | ---|
| `property` | String | The property you want to use to get the tasks. See the **Properties** section below.|
| `value` | String or Number | The value of the property without the quotation marks. Case-sensitive. Partial matches aren't supported. 

## Properties
The `property` parameter can take the following values:

| Property name | Type | Description |
| ------- | -------| ------ |
| `user_id` | Number | The unique ID of the user to whom the task is assigned |
| `title` | String | The title of the task without the quotation marks |
| `description` | String | The long description of the task without the quotation marks|
| `due_date` | String | The date and time when the task is due. Must be in the [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. For example, `2024-04-02T15:00`. |
| `warning` | Number | The number of minutes before the `due_date` when the assigned user of the task should be alerted. Represented as a negative number. For example, `-30` alerts the user 30 mins before the due date.|
| `id` | Number | The unique ID of the task |

## Example

### Request

```
{base_url}/tasks?title=Piano recital
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
## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

