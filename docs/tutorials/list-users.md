---
layout: default
title: List users
parent: Tutorials
nav_order: 4
---

**On this page:**

- TOC
{:toc}

# List all or some users: a tutorial

This tutorial should take you about 15 minutes to complete.

## Before you begin

1. Make sure you've [set up your environment](./set-up-dev-env.md).
2. [Start the Orca Sightings service](./start-service.md) with `json-server`.

## How to list all users

**To use cURL:**

1. Open a new terminal window.
2. Run the following command:

```shell
curl -X GET http://localhost:3000/users/
```

**To use Postman:**

1. In Postman's main panel on the right, toward the top, select **GET**.
2. Add the following content to the URL text box next to GET: `http://localhost:3000/users/`.
3. Click **Send**.

## View the response

The response body should show all users and look like this:

```json
[
  {
    "last_name": "Marsh",
    "first_name": "Stan",
    "email": "stan.marsh@gmail.com",
    "id": 1
  },
  {
    "last_name": "Broflovski",
    "first_name": "Kyle",
    "email": "kyle.broflovski@yahoo.com",
    "id": 2
  },
  {
    "last_name": "Cartman",
    "first_name": "Eric",
    "email": "eric.cartman@hotmail.com",
    "id": 3
  },
  {
    "last_name": "McCormick",
    "first_name": "Kenny",
    "email": "kenny.mccormick@gmail.com",
    "id": 4
  }
]
```

In Postman, you should also see a green 200 OK message at the top of the pane. Hover over that text to see the full confirmation message.

That's it. Next, view the reference topic [`GET /users`](../reference/users/users-get.md) to see an example of listing a specific user by its `id`.

Also, you can try other [tutorials](./tutorials.md) like [adding a user](./add-user.md) or view other topics in the [API reference](../reference/api-reference.md).
