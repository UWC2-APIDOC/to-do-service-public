---
layout: page
---

# Getting Started with the To-Do-Service API

## Simplify Task Management with the To-Do-Service

The To-Do service provides a cloud-hosted to-do list using which the subscribers can post their tasks and receive reminders for those tasks.

Get familiar with the To-Do-Service and experience how easy it is to integrate and the API's task management features. Create a new task and see firsthand the value the To-Do-Service API can add to your applications.

---

### QuickStart

#### Step 1: Set Up Your Development Environment

Before you start using the To-Do-Service, set up your development environment. Follow these simple steps to get started:

1. **Install Necessary Tools**: Ensure you have a system with Windows, Linux, or iOS. Install Postman or curl for making API requests.
2. **Base URL**: For local testing, use `http://localhost:3000` as your {base_url}.

#### Step 2: Post Your First Task

Let’s dive in with a simple hands-on exercise to post your first task.

##### Using Postman

1. **Open Postman**: Launch the Postman application.
2. **Create a New Request**: Click **New** and select **Request**.
3. **Set Request Type and URL**: Set the request type to `POST` and the URL to `http://localhost:3000/tasks`.
4. **Set Headers**:
   - Key: `Content-Type`, Value: `application/json`
5. **Set Body**: Select the **Body** tab, set the body to JSON, and then, paste the following:

    ```json
    [
      {
        "user_id": 1,
        "title": "Week 8 Assignment",
        "description": "Submit week 8 assignment",
        "due_date": "2024-05-21T23:59",
        "warning": -30
      }
    ]
    ```

6. **Send Request**: Click **Send** and check the response. You should see a response similar to:

    ```json
    [
      {
        "user_id": 1,
        "title": "Week 8 Assignment",
        "description": "Submit week 8 assignment",
        "due_date": "2024-05-23T23:59",
        "id": 1
      }
    ]
    ```

##### Using Curl

1. **Open Terminal**: Launch your terminal or command prompt.
2. **Execute Curl Command**: Run the following command to post your first task:

    ```bash
    curl -X POST http://localhost:3000/tasks \
    -H "Content-Type: application/json" \
    -d '[
      {
        "user_id": 1,
        "title": "Week 8 Assignment",
        "description": "Submit week 7 assignment",
        "due_date": "2024-05-14T23:59",
        "warning": -30
      }
    ]'
    ```

3. **Check the Output**: You should see a response similar to:

    ```json
    [
      {
        "user_id": 1,
        "title": "Week 8 Assignment",
        "description": "Submit week 7 assignment",
        "due_date": "2024-05-14T23:59",
        "id": 1
      }
    ]
    ```

---

### What’s Next?

Explore more features and tutorials:

- **Enroll a New User**: [Enroll a User](../tutorials/enroll-a-new-user.md)
- **Get Tasks for a User**: [Get Tasks for a User](../tutorials/get-tasks-for-a-user.md)
- **Update a Tasks**: [Update a Task](../tutorials/update-a-task.md)

---

### Additional Resources

- **[Overview](../index.md)**: Comprehensive guides and examples to help you integrate our API.
- **API Reference**: In-depth technical details and endpoint specifications.
  - [Task Resource](../api/task.md)
  - [User Resource](../api/user.md)
