---
layout: default
title: Set up your dev environment
parent: Tutorials
nav_order: 1
---

**On this page:**

- TOC
{:toc}

# Set up your development environment: a tutorial

> Adapted from [To-do service API: Before you start a tutorial](https://uwc2-apidoc.github.io/to-do-service-sp25/before-you-start-a-tutorial.html).

## Overview

Before you begin using the Orca Sightings service, you must set up your development environment.

Expect this to take about 30 minutes to complete.

## Step 1: Install the required software

Install the following software on your desktop, which should run a recent version of Windows, macOS, or Linux.

- A recent version of **[node.js](https://nodejs.org/en)**.
- A recent version of **[json-server](https://www.npmjs.com/package/json-server)**.
- The [**Postman desktop app**](https://www.postman.com/downloads/). You’ll run the Orca Sightings service on your local development system, so the web version of Postman won’t work. The default port for localhost is 3000: `http://localhost:3000/`

## Step 2: Download the relevant files from GitHub

Download a current copy of the **database file** and the relevant **startup script**. You can [download these from the Orca Sightings service repository on GitHub](https://github.com/juliebro/orca-sightings-api/tree/main/api).

To download each file:

1. Hover over a filename and click the link that appears.
2. On the upper right side of the panel, click the download button, a down arrow.
3. Do this for the `orca-sightings-db.json` file and one of the startup scripts: `orca-sightings.sh` for macOS and Linux or  `start-server.bat` for Windows.

## Step 3: Run JSON Server with the `orca-sightings-db.json` file

1. Go to the directory on your computer where you downloaded `orca-sightings-db.json` and the relevant start script.
2. On Windows, double-click the `start-server.bat` file to start the service. On macOS or Linux, open a terminal window, `cd` to the directory where you downloaded the files, and type `./orca-sightings.sh`. That runs the script in the current directory. If that doesn't work, type `json-server orca-sightings-db.json`. You should see some text like this that shows the service is running:

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

If you see the list of users from the service, you're ready to start the [Tutorials](./tutorials/tutorials.md).
