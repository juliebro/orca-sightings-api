---
layout: default
title: Get started by listing orca sightings
parent: Tutorials
nav_order: 3
---

**On this page:**

- TOC
{:toc}

# Get started by listing orca sightings: a tutorial

This tutorial shows you how to download the API files and try one of the service actions: viewing all orca sightings reported in the app for the San Juan Islands. If you've already [set up your environment](./set-up-dev-env.md), the process should take about 20 minutes.

## Step 1: Make sure you have the API database file

If you haven't already done so:

1. Download `orca-sightings-db.json`. The file is at [orca-sightings-api repo on GitHub](https://github.com/juliebro/orca-sightings-api/tree/main/api). This is a JSON file containing example users and sightings.
2. Copy this file into the same location as your `json-server` app.

## Step 2: Start JSON Server with the Orca Sightings service

To start the Orca Sightings service:

1. Open a terminal window and `cd` to the location of the `json-server` app.
2. Start the service by typing `json-server orca-sightings-db.json`. The service starts and lists some information to show it's running.

```shell
 user@macbookair ~ % json-server orca-sightings-db.json

  \{^_^}/ hi!

  Loading orca-sightings-db.json
  Done

  Resources
  http://localhost:3000/users
  http://localhost:3000/sightings

  Home
  http://localhost:3000

```

## Step 3: List orca whale sightings

In this part of the tutorial, you'll use cURL or Postman to list all orca whale sightings.

**To use cURL:**

1. Open a new terminal window.
2. Run this command:

```shell
curl -X GET http://localhost:3000/sightings
```

**To use Postman:**

1. In Postman's main panel on the right, toward the top, select **GET**.
2. Add the following content to the URL text box next to GET: `http://localhost:3000/sightings/`.
3. Click **Send**.

## Step 4: View the response

The response pane should show all sightings and look like this:

```json
[
    {
        "id": 1,
        "user_id": 1,
        "pod": "J-pod",
        "time": "2025-05-03T10:00",
        "location": "Lime Kiln Point State Park"
    },
    {
        "id": 2,
        "user_id": 3,
        "pod": "T49A",
        "time": "2025-05-01T19:00",
        "location": "Patos Island"
    },
    {
        "id": 3,
        "user_id": 4,
        "pod": "unknown",
        "time": "2025-04-28T12:30",
        "location": "Shaw Island"
    },
    {
        "id": 4,
        "user_id": 3,
        "pod": "K-pod",
        "time": "2025-02-15T10:00",
        "location": "Lime Kiln Point State Park"
    },
    {
        "id": 5,
        "user_id": 2,
        "pod": "J-pod",
        "time": "2025-01-20T13:00",
        "location": "Lime Kiln Point State Park"
    },
    {
        "id": 6,
        "user_id": 1,
        "pod": "K-pod",
        "time": "2024-12-24T17:15",
        "location": "Friday Harbor"
    },
    {
        "id": 7,
        "user_id": 4,
        "pod": "T49A",
        "time": "2025-12-13T06:00",
        "location": "Reuben Tarte County Park"
    },
    {
        "id": 8,
        "user_id": 2,
        "pod": "T49A",
        "time": "2025-01-30T11:00",
        "location": "Lime Kiln Point State Park"
    }
]
```

In Postman, you should also see a green 200 OK message at the top of the pane. Hover over that text to see the full confirmation message.

That's it. Next, view the reference topic [`GET /sightings`](../reference/sightings/sightings-get.md) to see an example of listing a specific sighting by its `id`.

You can also try other [tutorials](./tutorials.md) like [adding a user](./add-user.md) or view other topics in the [API reference](../reference/api-reference.md).
