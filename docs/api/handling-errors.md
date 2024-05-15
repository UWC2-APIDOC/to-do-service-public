---
layout: page
---

# Handling Errors in the To-Do Service API

The To-Do service API follows standard HTTP status codes to indicate the success or failure of an API call. Here is an overview of common HTTP status codes and their meanings, along with typical reasons for each code.

Operations that execute successfully will return `2xx` codes. Operations that result in an error due to a problem on the client's side, such as invalid input, will return standard `4xx` codes. Operations that result in an error due to a problem with the server will return `5xx` codes.

## HTTP Status Code Summary

This section summarizes the most frequent HTTP status codes returned by the API and describes their common causes.

| **HTTP Status Code** | Status Text           | Description                                                                                                                                                                 | Common Causes                                                                                                                                             |
| -------------------- | --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **200**              | OK                    | The request succeeded. The exact result depends on the HTTP method used. With `GET`, the requested resource is returned. With `POST`, a new resource is created or updated. | N/A                                                                                                                                                       |
| **400**              | Bad Request           | The request was unacceptable, often due to missing a required parameter or malformed request body.                                                                          | Missing required parameters, malformed JSON, or invalid data formats.                                                                                     |
| **404**              | Not Found             | The requested resource does not exist.                                                                                                                                      | Incorrect endpoint URL, attempting to access non-existent resources, or typo in the request.                                                              |
| **405**              | Method Not Allowed    | The HTTP method used is not supported by the endpoint.                                                                                                                      | Using an inappropriate HTTP method, like sending `GET` instead of `POST`, or trying to delete where only updates are allowed.                             |
| **500**              | Internal Server Error | The server encountered an unexpected condition that prevented it from fulfilling the request.                                                                               | A generic server-side issue, such as a crash, unhandled exceptions, or resource constraints.                                                              |
| **503**              | Service Unavailable   | The server cannot handle the request.                                                                                                            | Server is temporary overloaded or insufficient resources to process the request.                                                                          |
| No Status code       | ECONNREFUSED          | The service refused the connection.                                                                                                                                         | The service is offline, or you're connecting to the wrong port or hostname. Check if the service is running and try again with the correct port/hostname. |
