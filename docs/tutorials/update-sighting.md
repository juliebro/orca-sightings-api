---
layout: default
title: Update a sighting
parent: Tutorials
nav_order: 9
---

{: .comment }
This page is in progress.

**On this page:**

- TOC
{:toc}

# Update a sighting: a tutorial

This tutorial should take you about 25 minutes to complete.

Also see the API reference pages:

- [PUT /sightings](../reference/sightings/sightings-put.md)
- [PATCH /sightings](../reference/sightings/sightings-patch.md)

## Before you begin

1. Make sure you've [set up your environment](./set-up-dev-env.md).
2. If it's not already running, [start the Orca Sightings service](./start-service.md) with json-server.

## How to update the full sighting entry

Use the PUT method to update a full sighting entry.

### Step 1: list all sightings to find the `id` of the sighting you want to update

You can use cURL or Postman to submit a PUT request.

**To use cURL:**

1. Open a new terminal window.
2. [List all sightings](./list-sightings.md). Notice the sighting entry with an `id` of `1`.
3. Include that information in a cURL request, changing the first name to `Ken` and the email to `ken.mccormick@gmail.com`:

```shell
curl -X PUT \
  -H "Content-Type: application/json" \
  -d '{
    "user_id": 1,
    "pod": "K-pod",
    "time": "2025-05-03T10:30",
    "location": "Lime Kiln Point State Park"
  }' \
  http://localhost:3000/sightings/1
```

In the cURL command, `-X` denotes the method to use, `-H` indicates the header to use, and `-d` specifies the data to include. The `4` at the end of the URL specifies the sighting ID.

{: .tip }
The `user_id` isn't the same as the `id`. The latter refers to the sighting ID, which you add to the end of the URL. The former pairs the sighting with the user who reported the sighting.

**To use Postman:**

1. Open Postman.
2. [List all sightings](./list-sightings.md). 
3. In the this example, you'll choose **??**. Notice that this sighting has an `id` of `1`. You'll use that value later on.

```json
???
```

### Step 2: replace the entire entry using the PUT method

1. In Postman's main panel on the right, toward the top, select **PUT**.
2. Add the following content to the URL text box next to PUT: `http://localhost:3000/users/4`. This indicates that you'll replace the information for the user that has an ID of 4.
3. If you don't already have the header designated, choose **Headers** and specify **Content-Type: application/json**.
4. Choose **Body** and specify **Raw**.
5. Copy the following example code that changes the name **Kenny** to **Ken** in the `first_name` and `email` properties. Paste this into Postman's **Body** text box.

```json
{
   "last_name": "McCormick",
   "first_name": "Ken",
   "email": "ken.mccormick@gmail.com"
}
```

{: .note }
Notice that you don't need the ID. Enter it in Postman's URL parameters. You must remove the trailing comma in the last key-value pair.

Notice that the response includes the entire entry details with the ID.

```json
{
  "last_name": "McCormick",
  "first_name": "Ken",
  "email": "ken.mccormick@gmail.com",
  "id": 4
}
```

## How to update only part of the entry

Update just a part of the user entry using the PATCH method. We'll choose the user with an `id` of `1` to update.

**To use cURL:**

Send a request using cURL with the following command:

```shell
curl -X PATCH \
     -H "Content-Type: application/json" \
     -d '{ "email": "stan@example.com" }' \
     http://localhost:3000/users/1
```

Notice that the response includes the entire entry details with the updated email.

```shell
{
    "last_name": "Marsh",
    "first_name": "Stan",
    "email": "stan@example.com",
    "id": 1
}
```

**To use Postman:**

1. In Postman's main panel on the right, toward the top, select **PATCH**.
2. Add the following content to the URL text box next to PATCH: `http://localhost:3000/users/1`. This indicates that you'll update some information for the user that has an ID of 1.
3. If you don't already have the header designated, choose **Headers** and specify **Content-Type: application/json**.
4. Choose **Body** and specify **Raw**.
5. Copy the following example code that changes the email **stan.marsh@gmail.com** to **stan@example.com** in the `email` property. Paste this into Postman's **Body** text box.

```json
{
   "email": "stan@example.com"
}
```

Notice that the response includes the entire entry details with the updated email.

```json
{
    "last_name": "Marsh",
    "first_name": "Stan",
    "email": "stan@example.com",
    "id": 1
}
```

You've completed this tutorial. Next try other [tutorials](./tutorials.md) or refer to the [PUT](../reference/users/users-put.md) and [PATCH](../reference/users/users-patch.md) reference topics.
