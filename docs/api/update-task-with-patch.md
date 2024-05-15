---
layout: page
---

# Update a task with PATCH

Use `PATCH` to update a task when you want to change only some of the information in that task. You must supply the task `id` in both the request endpoint and the request body. 

## Endpoint

The endpoint for using `PATCH` to update a task is:

```
{server_url}/tasks/{id}
```

## Properties

The following example contains a request body for a `PATCH` request.

```json
{
  "user_id": 3,
  "title": "Get shots for cat", 
  "description": "Annual vaccinations for Sophie", 
  "due_date": "2024-05-15T14:00", 
  "warning": "-20",
  "id": 4
}
```

## Descriptions

The following table defines properties in the request body.

| Property name | Type   | Description                                                                                                                                                 |
| ------------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `user_id`     | Number | The ID of the user resource to which this task is assigned.                                                                                                 |
| `title`       | String | The title or short description of the task.                                                                                                                 |
| `description` | String | The long description of the task.                                                                                                                           |
| `due_date`    | String | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the task is due.                                                         |
| `warning`     | Number | The number of minutes relative to the `due_date` to alert the user of the task. This is normally a negative number to alert the user before the `due_date`. |
| `id`          | Number | (Required) The task's unique record. ID.                                                                                                                     |
## Operations

When you use `PATCH` to update a task, you can:

* **Update an entire task** — Replace the entire request body.
* **Update part of a task** — Only replace the fields to update; omit the others. 

> ℹ️ Task `id` is required in both scenarios and must match in both the endpoint and the request body. For example, if you change the `id` in only the request body, the service returns a `200 OK`, but does not update the task. 

## Examples

Use the following examples when sending `PATCH` requests to the To-Do service.

### cURL

```bash
curl --location --request PATCH '{server_url}:{port}/tasks/4' \
--header 'Content-Type: application/json' \
--data '{
  "user_id": 3,
  "title": "Title of my task",
  "description": "Name of my task",
  "due_date": "2024-05-15T14:00",
  "warning": "-20",
  "id": 4
}'
```

### Complete task body

```json
{
  "user_id": 3,
  "title": "Get shots for my cat", 
  "description": "Annual vaccinations for Sophie", 
  "due_date": "2024-05-15T14:00", 
  "warning": "-20",
  "id": 4
}
```
### Partial task body

```json
{
  "description": "Annual vaccinations for Zeke",
  "id": 4
}
```
## Related topics

- [Task resource](task.md)
- [Handling errors](handling-errors.md)