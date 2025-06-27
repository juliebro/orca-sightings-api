---
layout: default
title: Add a new sighting
parent: Tutorials
nav_order: 8
---

**On this page:**

- TOC
{:toc}

# Add a new sighting to the Orca Sightings service: a tutorial

This tutorial should take you about 15 minutes to complete.

## Before you begin

Make sure you've [set up your environment](./set-up-dev-env.md) and [started the service using `json-server`](./start-service.md).

## Step 1: Submit a cURL or Postman request with the POST method

**To use cURL:**

Enter the following command to add a new sighting reported by the user with an `id` of `1`.

```shell
curl -X POST \
     -H "Content-Type: application/json" \
     -d '{ "user_id": 1, "pod": "K-pod", "time": "2024-12-24T09:20", "location": "Friday Harbor" }' \
     http://localhost:3000/sightings
```

In this example, -X specifies the method, -H indicates the header, and -d specifies the data.

For `user_id`, you specify `1` to pair the sighting with the first user. This is the person who reported the sighting.

Try using GET to see user 1:

```shell
curl -X GET http://localhost:3000/users/1
```

The result shows the user as Stan Marsh:

```json
{
    "last_name": "Marsh",
    "first_name": "Stan",
    "email": "stan.marsh@gmail.com",
    "id": 1
}
```

**To use Postman:**

1. Select **POST** and enter  `http://localhost:3000/sightings/`.
2. In the **Header** tab, select **Content-Type** and then **application/json**.
3. In the request body, select **Body > raw > JSON** and enter:

```json
{ 
    "user_id": 1, 
    "pod": "K-pod", 
    "time": "2024-12-24T09:20", 
    "location": "Friday Harbor" 
}
```

## Step 2: Make sure the service created the new sighting

Both of the previous examples should return the information from the request body plus a unique ID.

```json
{ 
    "user_id": 1, 
    "pod": "K-pod", 
    "time": "2024-12-24T09:20", 
    "location": "Friday Harbor",
    "id": 6
}
```

{: .note }
The `id` might be different if you've completed other tutorials first.

You've completed this tutorial. Next, try other [tutorials](./tutorials.md) or refer to the reference topic [POST /sightings](../reference/sightings/sightings-post.md).
