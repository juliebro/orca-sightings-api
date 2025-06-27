---
layout: default
title: Set up your environment
parent: Tutorials
nav_order: 1
---

**On this page:**

- TOC
{:toc}

# Set up your environment: a tutorial

> Adapted from [To-do service API: Before you start a tutorial](https://uwc2-apidoc.github.io/to-do-service-sp25/before-you-start-a-tutorial.html).

## Overview

Before you begin using the Orca Sightings service, you must set up your environment.

Expect this to take about 30 minutes to complete.

## Step 1: Install the required software

Install the following software on your desktop, which should run a recent version of Windows, macOS, or Linux.

- A recent version of **[node.js](https://nodejs.org/en)**.
- A recent version of **[json-server](https://www.npmjs.com/package/json-server)**.
- The [**Postman desktop app**](https://www.postman.com/downloads/). You’ll run the Orca Sightings service on your local development system, so the web version of Postman won’t work. The default port for localhost is 3000: `http://localhost:3000/`

## Step 2: Download the database file from GitHub

Download a current copy of the database file `orca-sightings-db.json` from [the Orca Sightings service repository on GitHub](https://github.com/juliebro/orca-sightings-api/tree/main/api).

To download the file:

1. Hover over `orca-sightings-db.json` and click the link that appears.
2. On the upper right side of the panel, click the download button, a down arrow.
3. Copy this file to the same location as your `json-server` app.

## Step 3: Run JSON Server with the `orca-sightings-db.json` file

To start the Orca Sightings service:

1. Open a terminal window and `cd` to the location of the `json-server` app.
2. Start the service by typing `json-server orca-sightings-db.json`. The service starts and lists some information to show it's running.

You should see some text like this that shows the service is running:

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

## Step 4: Make a test call to the service

Use cURL or Postman to test the service.

### Using cURL

```shell
curl -X GET http://localhost:3000/users/4
```

### Using Postman

1. Open Postman.
2. At the top of the right pane, select **GET**.
3. Next to **GET**, type `http://localhost:3000/users`.

If the service is running correctly, you should see a list of all existing users.

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

## Troubleshooting

If you receive an error in any step of the procedure, investigate, and correct the error before continuing. Some common situations that cause errors include:

- You mistyped a command.
- You aren't in the correct directory.
- A required software component didn't install correctly.
- A required software component isn't up to date.

If you see the list of users from the service, you're ready to start the [Tutorials](./tutorials.md).
