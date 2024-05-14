---
layout: page
---

# To-Do Service API Documentation

Welcome to the To-Do Service API documentation. This API simulates the REST interface of an imaginary task management service, providing a cloud-hosted task list through which subscribers can manage their tasks and receive reminders.

## Table of Contents

<!-- no toc -->
1. [Overview](#overview)
2. [Quickstart](#quickstart)
3. [Tutorials](#tutorials)
4. [API Reference](#api-reference)
5. [Support and Feedback](#support-and-feedback)

## Overview

The To-Do Service API allows developers to interact with a task management system programmatically. This API enables you to create, update, delete, and retrieve tasks, as well as manage user information. It is designed to be intuitive and easy to integrate into your existing applications.

Key features:

* Create and manage tasks
* User management
* Task categorization
* Search and filter capabilities

## Quickstart

Getting started with the To-Do Service API is simple. Follow these steps to post your first task:

1. **Set up your environment**: Ensure you setup your project using this [Before you start a tutorial](../tutorials/before-you-start-a-tutorial) guide.
2. **Send your first request**: Use the endpoint to create a task.

Example:

```sh
curl -X POST http://localhost:3000/tasks \
-H "Content-Type: application/json" \
-d '{
  "title": "My First Task",
  "description": "This is a test task"
}'
```

For more information and examples, see the [Tutorials](#tutorials) section below.

## Tutorials

Explore our step-by-step tutorials to perform common tasks with the To-Do Service API:

* Getting Started
    * [Before you start a tutorial](../tutorials/before-you-start-a-tutorial)
    * [Enroll a new user](../tutorials/enroll-a-new-user)
    * [Add a new task](../tutorials/add-a-new-task)

* Task Management
    * [Add a New Task](../tutorials/add-a-new-task)
    * [Update a Task](../tutorials/update-a-task.md)
    * [Delete a Task](../tutorials/delete-a-task)
    * [Delete Tasks by Due Date](../tutorials/delete-tasks-by-due-date)
    * [Find Tasks by User ID](../tutorials/find-tasks-by-user-id)
    * [Update a Task](../tutorials/update-a-task.md)
    * [Get Tasks by Title](../tutorials/get-tasks-by-title)

* User Management
    * [Enroll a new user](../tutorials/enroll-a-new-user)
    * [Update a User's Information](../tutorials/update-user-info)
    * [Update a User's Property](../tutorials/update-user-property)
    * [Update a User's Name](../tutorials/update_a_users_name.md)
    * [Get a User by Name](../tutorials/get-a-user-by-name)
    * [Get a User by ID](../tutorials/get-a-user-by-id)
    * [Search for a User](../tutorials/search-for-a-user.md)

## API Reference

The To-Do Service API is organized around REST. Our API has predictable resource-oriented URLs, accepts JSON-encoded request objects, returns JSON-encoded responses, and uses standard HTTP response codes, and verbs. The API reference docs refer to a `{base_url}` when they refer to the URL of a resource. The `{base_url}` value depends on the installation of the service.

* User Resource
    * [User Endpoints](user)
    * [Handling errors](handling-errors)

* Task Resource
    * [Task Endpoints](task)
    * [Handling errors](handling-errors)

* Endpoint Index
    * [All Endpoint Overview](endpoint-index)
    * [Properties Cheat Sheet](cs-for-successful-requests)

When running a local test, the `{base_url}` is generally:

```shell
http://localhost:3000
```

## Support and Feedback

For support or to provide feedback, please contact our [support team](mailto:support@yopmail.com) or visit our [community forum](mailto:community@yopmail.com).

Stay updated with the latest API changes by subscribing to our [newsletter](mailto:newsletter@yopmail.com).
