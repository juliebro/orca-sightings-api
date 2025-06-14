---
layout: default
title: Update a user
parent: Tutorials
nav_order: 5
---

**On this page:**

- TOC
{:toc}

# Update a user: a tutorial

{: .comment }
This page is in progress.

This tutorial should take you about 25 minutes to complete.

Also see the API reference pages:

- [PUT /users](../reference/users-resource/users-put.md)
- [PATCH /users](../reference/users-resource/users-patch.md)

## Before you begin

1. Make sure you've [set up your development environment](./set-up-dev-env.md).
2. [Start the Orca Sightings service](./start-service.md) with json-server.

## How to update the full user entry

In this part of the tutorial, you'll use the PUT method to update a full user entry.

1. Open Postman.
2. [List all users](./list-users.md) to find which one you want to update. In the this example, you'll choose **Kenny McCormick**. Notice that this user has an `id` of `4`. You'll use that value later on.

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

In this part of the tutorial, you'll replace the entire entry using the PUT method. 

1. In Postman's main panel on the right, toward the top, select **PUT**.
2. Add the following content to the URL text box next to PUT: `http://localhost:3000/users/4`. This indicates that you'll replace the information for the user that has an ID of 4.
3. If you don't already have the header designated, choose **Headers** and specify **Content-Type: application/json**.
4. Choose **Body** and specify **Raw**.
5. Copy the new example code that changes the name **Kenny** to **Ken** in the `first_name` and `email` properties. Paste this into Postman's **Body** text box.

{: .note }
Notice that you don't need the ID. You'll enter it in Postman's URL text box. You do need to remove the trailing comma in the last key-value pair.

```json
{
   "last_name": "McCormick",
   "first_name": "Ken",
   "email": "ken.mccormick@gmail.com"
 }
 ```

Notice that the response includes the entire entry details with the ID.

```json
{
  "last_name": "McCormick",
  "first_name": "Ken",
  "email": "ken.mccormick@gmail.com",
  "id": 4
 }
```

## How to update part of the entry

In this part of the tutorial, you'll update just a part of the user entry using the PATCH method.
