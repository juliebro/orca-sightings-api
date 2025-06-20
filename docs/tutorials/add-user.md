---
layout: default
title: Add a new user
parent: Tutorials
nav_order: 4
---

**On this page:**

- TOC
{:toc}

# Add a new user to the Orca Sightings service: a tutorial

This tutorial should take you about 15 minutes to complete.

## Before you begin

Make sure you've [set up your environment](./set-up-dev-env.md) and [started the service using `json-server`](./start-service.md).

## Step 1: Submit a cURL or Postman request with the POST method

**To use cURL:**

Enter the following command to add a new user named Ben Waters.

```shell
curl -X POST \
     -H "Content-Type: application/json" \
     -d '{ "last_name": "Waters", "first_name": "Ben", "email": "ben.waters@gmail.com" }' \
     http://localhost:3000/users
```

In this example, -X specifies the method, -H indicates the header, and -d specifies the data.

**To use Postman:**

1. Select **POST** and enter  `http://localhost:3000/users/`.
2. In the **Header** tab, select **Content-Type** and then **application/json**.
3. In the request body, select **Body > raw > JSON** and enter:

```json
{
  "last_name": "Waters",
  "first_name": "Ben",
  "email": "ben.waters@gmail.com"
}
```

## Step 2: Make sure the service created the new user

Both of the previous examples should return the information from the request body plus a unique ID.

```json
{
  "last_name": "Waters",
  "first_name": "Ben",
  "email": "ben.waters@gmail.com",
  "id": 5
}
```

{: .note }
The `id` might be different if you've completed other tutorials first.

You've completed this tutorial. Next, try other [tutorials](./tutorials.md) or refer to the reference topic [POST /users](../reference/users/users-post.md).
