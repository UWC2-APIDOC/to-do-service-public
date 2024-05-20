---
layout: page
---
# Build a User Task Management System with *To Do*

Turn your app into a daily to do list

## The basics

To Do is a cloud service that helps your customers stay on track by generating task reminders. The lightweight API provides access to To Do data and functionality, allowing developers to build custom features and branded interfaces. The To Do API uses REST and returns HTTP response codes and responses encoded in JSON.

There are two resources.

* **Users** - Individuals who sign up for your To Do service. Each user can have multiple tasks. The Users resource includes endpoints to create, retrieve, update, and delete user information.

* **Tasks** - Save To Do tasks here. Each task has details such as title, description, and due date. The Tasks resource includes endpoints to create, retrieve, update, and delete tasks.

## Benefits

* **Brandable** - Create a bespoke front end that syncs with your app and corporate branding.

* **Lightweight** - Registered users drive data input with easy-to-read forms, so expect a minimal impact on your customer support team.

* **Customer-focused** - Help your customers succeed and give them another reason to come back to your app and site.

## Getting help

Contact the [tech support](mailto:support@yopmail.com) or visit the [development portal](https://example.com/) to learn more.

## Support documentation

Sure! We have To Do docs.

* **Tutorials** - Guided instructions that show you how to use the service. Check out [the complete list of tutorials](#tutorials).

* **Reference guides** - Technical references describe how the service works and how to use it. We assume you have a basic understanding of key concepts. Here's a [sample](api/user).

## Quickstart

Ready to start? Check out our [quickstart guide](api/quickstart_sinead.html).

## Tutorials

Learn how to do common tasks within the To-Do service.

First, do this tutorial to set up your development system for these tutorials. You only have to do this one time per development system.

* [Before you start a tutorial](tutorials/before-you-start-a-tutorial.md)

After your system is ready, these tutorials show you how to perform common tasks.

* [Enroll a new user](tutorials/enroll-a-new-user)
* [Update a specific user's information](tutorials/update-user-info)
* [Add a new task](tutorials/add-a-new-task)
* [Add a new property to an existing task](tutorials/update-task-new-prop)
* [Change the due-date of a task (coming soon)](#tutorials)
* [Delete a task](tutorials/delete-a-task)
* [Get a user by name](tutorials/get-a-user-by-name)
* [Get tasks by title](tutorials/get-tasks-by-title)
* [Get tasks by a property](tutorials/get-task-by-property.md)
* [Get a user by email](tutorials/get-user-by-email)
* [Get tasks for a user](tutorials/get-tasks-for-a-user.md)
* [Update a task](tutorials/update-a-task.md)
* [Update a task description](tutorials/update-task-description.md)
* [Update a user property)](tutorials/update-user-property)

## API reference docs

Detailed descriptions of the service's resources.

The API reference docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When running a local test, the `{base_url}` is
generally `http://localhost:3000`.

* [user resource](api/user)
* [task resource](api/task)

* [Handling errors](api/handling-errors)
* [Get tasks by title](api/tasks-get-tasks-by-title.md)
* [Get tasks by property](api/get-task-ref.md)
