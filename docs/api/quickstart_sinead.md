---
layout: page
---

# Quickstart guide

Have you a lot on your plate to keep track of?

Easily manage all your tasks in one simple to-do list!

## At a glance

This Quickstart provides all the information you need to begin using To-Do to track your tasks.

You’ll learn when and how to use the web service and get set up to make your first call to the API.

## Setting up the To-Do service

Tasks will surface in the To-Do service when they are created in the database and assigned to users (by user {id}). If you’ve used the To-Do service previously, you’re already enrolled in the service and may have tasks to work with.

If not, you might need to set up your development system and get going from scratch. Don’t worry – you only have to do this one time per development system! Follow these [prerequisite steps](../tutorials/before-you-start-a-tutorial.md) to install the tools and test your development system.

## When to use the To-Do service

The To-Do service REST API offers a wide range of integration possibilities, from enhancing internal workflow to creating customer-facing task reminder apps.

The service comprises two resources: [`user`](user) and [`task`](task). The [`user`](user) resource (containing the subscribers to the service) works in synergy with the [`task`](task) resource (containing the tasks) to align users with their to-do list reminders.

Using this cloud-based service, customers can register themselves to create and manage their own tasks.
When they're registered, customers can update and delete tasks to suit their needs. Adding tasks on customers' behalf is easy - if they're collaborating with colleagues on different teams and projects, for example, they might be delegated requests and assigned tasks from different sources.

## How to use the To-Do service

To build your API call, you must have the following components:

* **A host.**  The {base_url} depends on users' installation of the service in their development environment. For v1 of To-Do Service API, the **base_url** variable is typically set to `http://localhost:3000`.
* **Authorization.**  For v1 of the To-Do service, requests do not use any authorization. All endpoints are available to all users and applications.
* **A request.**  The To-Do service REST API enables CRUD operations via HTTP requests on database resources (`GET`, `POST`, `PUT`, `PATCH`, and `DELETE` methods). Request and response bodies are encoded as JSON.

### Supported endpoints

| HTTP Method | Endpoint |
| :--------------: | :--------------: |
| GET | [List all users](users-get-all-users.md) |
| GET | [List user by ID](users-get-user-by-id.md) |
| GET | [List user by email](users-get-user-by-email.md) |
| POST | [Create a user](users-create-user.md) |
| PUT | [Update user by ID](users-update-by-id.md) |
| PATCH | [Update user email](users-change-user-email.md) |
| PATCH | [Update user properties](users-change-user-property.md) |
| GET | [Get task by title](tasks-ref-topic-get-task-by-title.md) |
| CREATE | [Create a task](tasks-create-task.md) |
| PATCH | [Update a task](update-task-with-patch.md) |

## Make your first API call – *List all tasks*

Assume that you’re already enrolled in the To-Do service and you want to list all tasks as a first call to the API.

Let’s test making this simple request to the [`task`](task) resource.  You’ll use cURL to make the API call.

```bash

curl http://localhost:3000/tasks
```

If the call was successful, the response you receive will be a list of tasks from the To-Do service such as you see in this example:

```js

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
  },
  {
    "user_id": 2,
    "title": "Oil change",
    "description": "5K auto service",
    "due_date": "2024-03-10T09:00",
    "warning": "-60",
    "id": "3"
  },
  {
    "user_id": 3,
    "title": "Get shots for dog",
    "description": "Annual vaccinations for poochy",
    "due_date": "2024-05-11T14:00",
    "warning": "-20",
    "id": "4"
  }

```

---

**NOTE:**
cURL comes installed by default on Mac operating systems. If you need to, install it from [here](https://curl.se/windows/).

---

## Next steps

Now that you’ve everything set up correctly, you’re good to go and can take full advantage of the To-Do service API! Go ahead and start posting new tasks or enrolling new users. You’ll see how easy the API is to use.

If you need more guidance, the Tutorials section of the API documentation walks through any task you’ll want to do. The finer details of the supported resources, endpoints and properties are in the API reference section. For more information, go [here](../index.md).
