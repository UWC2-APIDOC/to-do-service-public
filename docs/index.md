---
layout: page
---

# To-Do service API

This is a mock API to simulate the REST interface of an
imaginary service.

The To-Do service provides a cloud-hosted task list through which
subscribers can post tasks and receive reminders of those tasks.

## Alternate overviews

* [deullmer's overview](overview-daniel.md)
* [Anne M's overview](overview_annem.md)
* Get a comprehensive understanding of the tool by reading the [Overview](overview_sai)
* [Overview-mhull](api/overview_mhull.md)

## Quickstart

[Quickstart (SineadC)](api/quickstart_sinead.md)
[Get Started](api/get-started.md) with the To-Do service to see how easy it is to use!

## Tutorials

Learn how to do common tasks within the To-Do service.

First, do this tutorial to set up your development system for these tutorials. You only have to do this one time per development system.

* [Before you start a tutorial](tutorials/before-you-start-a-tutorial)

After your system is ready, these tutorials show you how to perform common tasks.

* [Enroll a new user](tutorials/enroll-a-new-user)
* [Update a specific user's information](tutorials/update-user-info)
* [Add a new task](tutorials/add-a-new-task.md)
* [Add a new property to an existing task](tutorials/update-task-new-prop)
* [Change the due-date of a task _(coming soon)_](#tutorials)
* [Delete a task](tutorials/delete-a-task)
* [Delete tasks by due date](tutorials/delete-tasks-by-due-date)
* [Get a user by name](tutorials/get-a-user-by-name)
* [Get tasks by title](tutorials/get-tasks-by-title.md)
* [Get tasks by a property](tutorials/get-task-by-property.md)
* [Get a user by email](tutorials/get-user-by-email)
* [Get tasks for a user](tutorials/get-tasks-for-a-user.md)
* [Find tasks by user ID](tutorials/find-tasks-by-user-id)
* [Update a task](tutorials/update-a-task.md)
* [Update a task description](tutorials/update-task-description.md)
* [Update a user property)](tutorials/update-user-property)
* [Update a user's email](tutorials/update-user-email)
* [Searching for users](tutorials/search-for-a-user.md)
* [How to update a user's name](./tutorials/update_a_users_name.md)
* [Get tasks by category](tutorials/get-tasks-by-category.md)

## API reference docs

Detailed descriptions of the service's resources.

The API reference docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When running a local test, the `{base_url}` is
generally `http://localhost:3000`.

* [user resource](api/user)
* [task resource](api/task)
* [Endpoint index](api/endpoint-index)
* [Handling errors](api/handling-errors)
* [Properties cheat sheet for successful requests](api/cs-for-successful-requests)
* [Get tasks by title](api/tasks-get-tasks-by-title.md)
* [Get tasks by property](api/get-task-ref.md)
* [Delete a task by ID](api/tasks-delete-by-id)
* [task category resource](api/tasks-category)
