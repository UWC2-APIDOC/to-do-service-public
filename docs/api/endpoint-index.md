# Endpoint index

An endpoint is a specific Uniform Resource Locator (URL), or _route_, in the API that you can use to perform certain actions or retrieve specific resources in the to-do-service.

This page lists all the endpoints and associated methods offered by the to-do-service.

| **Name**      | **Method** | **URL**                 |
| ------------- | ---------- | ----------------------- |
| Enroll a user | POST       | {server_url}/users/     |
| Get all users | GET        | {server_url}/users/     |
| Create a task | POST       | {server_url}/tasks/     |
| Update a task | PATCH      | {server_url}/tasks/{id} |
| Delete a task | DELETE     | {server_url}/tasks/{id} |
