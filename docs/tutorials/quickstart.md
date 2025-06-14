---
layout: default
title: Get started by listing orca sightings
parent: Tutorials
nav_order: 2
---

- TOC
{:toc}

# Get started by listing orca sightings: a tutorial

This tutorial shows you how to download the API files and try one of the service actions: viewing all of the orca sightings reported in the app for the San Juan Islands. If you've already [set up your development environment](set-up-dev-env.md), the process should take about 15 minutes.

## Step 1: Make sure you have the API files

The files are located in the [orca-sightings-api repo on GitHub](https://github.com/juliebro/orca-sightings-api/tree/main/api). The directory contains the following files:

- `orca-sightings-db.json`: a JSON file containing example users and sightings.
- `orca-sightings.sh`: a shell script that starts JSON Server. Use this for Linux or macOS.
- `orca-sightings.bat`: a batch file that starts JSON Server. Use this for Windows.

## Step 2: Start JSON Server with the Orca Sightings service

To start the Orca Sightings service:

1. Open a terminal window and `cd` to the location of the `json-server` app.

2. Make sure you intall the API files in the same directory. If they aren't copy or move them now.

3. Start the service by typing `json-server orca-sightings-db.json`. The service starts and lists some information to show it's running.

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

## Step 3: Use Postman to list orca whale sightings

In this part of the tutorial, you'll use Postman to list all orca whale sightings.

1. In Postman's main panel on the right, toward the top, select **PUT**.
2. Add the following content to the URL text box next to GET:
`http://localhost:3000/users/`
3. If you don't already have the header designated, choose **Headers** and specify **Content-Type: application/json**.
4. Click **Send**.

The response pane should look like this:

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