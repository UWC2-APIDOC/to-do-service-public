layout: page
---

# delete task

Delete a task from the to-do service. 

## URL

```shell

DELETE {server_url}/tasks/<task id>
```

## Request headers

This request does not use any authorization. The endpoint is available to all users and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Task | The task to be deleted. | Optional | application/json. Default value.  || 

## Request body

None


## Sample request

The DELETE request should look like this.

{server_url}/tasks/<task id>

It uses the **DELETE** method and returns a the response shown in the **Return body**.



## Return body
The following example shows the response. 
```js
[]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 201 | Deleted | Task deleted successfully. |
| 500 | Internal server Error | Invalid JSON. |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

