---
layout: page
---

# To-Do service API

The To-Do service provides an simple REST API to create and manage tasks. You can configure reminders for your tasks so you never forget an important date, event, or job again.  

Administrators can manage users or allow users to subscribe or unsubscribe with a minimum of oversight.

Need help? The To-Do service has extensive [user documentation](https://uwc2-apidoc.github.io/to-do-service-public/).

**NOTE:** This is a mock API to simulate the REST interface of an
imaginary service.

## Quickstart

Get started right away with the following tutorials:

* [System set up for PC](tutorials/before-you-start-a-tutorial.md) and [Mac](./tutorials/macos-installation.md)
* [Create a new user](tutorials/enroll-a-new-user)
* [Create a new task](tutorials/add-a-new-task)

## Tutorials

Learn how to use the To-Do service.

First, complete this tutorial to set up your development system. You only have to do this one time per development system.

* [System set up for PC](tutorials/before-you-start-a-tutorial.md) and [Mac](./tutorials/macos-installation.md)
After your system is ready, these tutorials show you how to perform common actions.

* [Create a new user](tutorials/enroll-a-new-user)
* [Update a user](tutorials/update-user-info)
* [Create a new task](tutorials/add-a-new-task)
* [Update an existing task](tutorials/update-task-new-prop)
* [Delete a task](tutorials/delete-a-task)
* [Get a user by name](tutorials/get-a-user-by-name)
* [Get tasks by title](tutorials/get-tasks-by-title)
* [Get tasks by a property](tutorials/get-task-by-property.md)
* [Get a user by email](tutorials/get-user-by-email)
* [Get tasks for a user](tutorials/get-tasks-for-a-user.md)

## API Reference

Detailed descriptions of the service's resources. The `task` and `user` resources support get, update, patch, delete, and search.

The API reference docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When running a local test, the `{base_url}` is
generally `http://localhost:3000`.

* [User resource](api/user)
* [Create user](api/users-create-user.md)
* [Update user](api/users-change-user-property.md)
* [Get users](api/users-get-all-users.md)
* [Task resource](api/task)
* [Create task](api/tasks-create-task.md)
* [Get tasks by property](api/get-task-ref.md)
* [Update task](api/update-task-with-patch.md)
* [Delete task](api/tasks-delete-task.md)

## Troubleshooting and support

See the following topics for help:

* Review environment setup for [PC](./tutorials/before-you-start-a-tutorial.md) and [Mac](./tutorials/macos-installation.md)
* [Error handling](api/handling-errors.md)
* [User documentation](https://uwc2-apidoc.github.io/to-do-service-public/)
