---
layout: default
title: Update a sighting
parent: Tutorials
nav_order: 9
---

**On this page:**

- TOC
{:toc}

# Update a sighting: a tutorial

This tutorial should take you about 20 minutes to complete.

## Before you begin

1. Make sure you've [set up your environment](./set-up-dev-env.md).
2. If it's not already running, [start the Orca Sightings service](./start-service.md) with json-server.

## How to update the full sighting entry

Use the PUT method to update a full sighting entry.

### Step 1: list all sightings to find the `id` of the sighting you want to update

You can use cURL or Postman to submit a PUT request.

**To use cURL:**

1. Open a new terminal window.
2. [List all sightings](./quickstart.md#step-3-list-orca-whale-sightings). Notice the sighting entry with an `id` of `2`.

```json
...
{
  "id": 2,
  "user_id": 3,
  "pod": "T49A",
  "time": "2025-05-01T19:00",
  "location": "Patos Island"
},
...
```

**To use Postman:**

1. Open Postman.
2. [List all sightings](./quickstart.md#step-3-list-orca-whale-sightings). Notice the sighting entry with an `id` of `2`.

```json
...
{
  "id": 2,
  "user_id": 3,
  "pod": "T49A",
  "time": "2025-05-01T19:00",
  "location": "Patos Island"
},
...
```

### Step 2: replace the entire entry using the PUT method

**To use cURL:**

1. Include that information in a cURL request, changing the pod to `unknown`. Don't include the `id` in the `-d` field. Instead, include that number at the end of the URL. This is the *endpoint*.

```shell
curl -X PUT \
  -H "Content-Type: application/json" \
  -d '{
    "user_id": 3,
    "pod": "unknown",
    "time": "2025-05-01T19:00",
    "location": "Patos Island"
  }' \
  http://localhost:3000/sightings/2
```

In the cURL command, `-X` denotes the method to use, `-H` indicates the header to use, and `-d` specifies the data to include.

{: .tip }
The `user_id` isn't the same as the `id`. The latter refers to the sighting ID, which you add to the end of the URL. The former pairs the sighting with the user who reported it.

The output should look like the following:

```shell
{
  "user_id": 3,
  "pod": "unknown",
  "time": "2025-05-01T19:00",
  "location": "Patos Island"
  "id": 2,
}
```

**To use Postman:**

1. In Postman's main panel on the right, toward the top, select **PUT**.
2. Add the following content to the URL text box next to PUT: `http://localhost:3000/sightings/2`. This indicates that you'll replace the information for the user that has an ID of 2.
3. If you don't already have the header designated, choose **Headers** and specify **Content-Type: application/json**.
4. Choose **Body** and specify **Raw**.
5. Copy the following example code that changes the pod to `unknown.` Paste this into Postman's **Body** text box.

```json
{
  "user_id": 3,
  "pod": "unknown",
  "time": "2025-05-01T19:00",
  "location": "Patos Island"
}
```

{: .note }
Notice that you don't need the ID. Enter it in Postman's URL parameters. You must remove the trailing comma in the last key-value pair.

Notice that the response includes the entire entry details with the ID.

```json
{
  "user_id": 3,
  "pod": "unknown",
  "time": "2025-05-01T19:00",
  "location": "Patos Island"
  "id": 2,
}
```

## How to update only part of the entry

Update just a part of the user entry using the PATCH method. Choose the same sighting as in the previous example with an `id` of `2`. You'll update just the time.

**To use cURL:**

Send a request using cURL with the following command:

```shell
curl -X PATCH \
     -H "Content-Type: application/json" \
     -d '{ "time": "2025-05-01T08:00" }' \
     http://localhost:3000/sightings/2
```

Notice that the `time` value, which follows the `T` is now 8:00 AM: `08:00`.

{: .note}
For a full description of the time value, refer to [ISO 8601 format](../reference/sightings/iso-8601-format.md).

Notice that the response includes the entire entry details with the updated time.

```shell
{
  "user_id": 3,
  "pod": "unknown",
  "time": "2025-05-01T08:00",
  "location": "Patos Island"
  "id": 2,
}
```

**To use Postman:**

1. In Postman's main panel on the right, toward the top, select **PATCH**.
2. Add the following content to the URL text box next to PATCH: `http://localhost:3000/sightings/2`. This indicates that you'll update some information for the sighting that has an ID of `2`.
3. If you don't already have the header designated, choose **Headers** and specify **Content-Type: application/json**.
4. Choose **Body** and specify **Raw**.
5. Copy the following example code that changes the time `...T19:00` to 8:00 AM: `...T08:00`. Paste the following into Postman's **Body** text box.

```json
{
   "time": "2025-05-01T08:00"
}
```

Notice that the response includes the entire entry details with the updated time.

```json
{
  "user_id": 3,
  "pod": "unknown",
  "time": "2025-05-01T08:00",
  "location": "Patos Island"
  "id": 2,
}
```

You've completed this tutorial. Next try other [tutorials](./tutorials.md) or refer to the [PUT](../reference/sightings/sightings-put.md) and [PATCH](../reference/sightings/sightings-patch.md) reference topics.
