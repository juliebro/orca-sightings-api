---
layout: default
title: Set up your development environment
parent: Tutorials
nav_order: 1
---

# Set up your development environment: a tutorial

*Adapted from [To-do service API: Before you start a tutorial](https://uwc2-apidoc.github.io/to-do-service-sp25/before-you-start-a-tutorial.html)*

## Overview

Before you begin using the Orca Sightings service, you must set up your development environment.

Expect this to take about 20 minutes to complete.

## Step 1: Create a GitHub user account

You’ll need a GitHub account. If you don’t already have one, create one at [GitHub](https://github.com/).

## Step 2: Install the required software

Install the following software on your desktop, which should run a recent version of Windows, macOS, or Linux.

- **[GitHub Desktop](https://github.com/apps/desktop)**
- A recent version of **[node.js](https://nodejs.org/en)**
- A recent version of **[json-server](https://www.npmjs.com/package/json-server)**
- A current copy of the **database file** and the relevant **startup script**. You can get these by syncing your fork. They’re located in the `/api` directory.
- The [**Postman desktop app**](https://www.postman.com/downloads/). You’ll run the Orca Sightings service on your development system with an `http://localhost` host name, so the web version of Postman won’t work.

## Step 3: Fork the repository

1. Go to https://github.com/juliebro/orca-sightings-api.
2. Click the **Fork** button on the right side of the page, near the top.

## Step 4: Clone the repository

Using GitHub Desktop, clone a repository to the workspace on your desktop.

1. Go to **File** > **Clone Repository**.
2. Select the **URL** tab.
3. Enter the URL for the Orca Sightings API: `https://github.com/juliebro/orca-sightings-api`
4. Click **Clone**.

## !! **Test your development system**

To test your development system:.

1. Create and check out a test branch of your fork of the Orca Sightings repository. In the below example, `<path to orca-sightings-api repo>` is where you cloned the **orca-sightings-api** repository to.

   ```text
   cd <path to orca-sightings-api repo>
   ls
   # (see the to-do-service directory in the list)
   cd to-do-service-sp25
   git checkout -b tutorial-test
   cd api
   json-server -w to-do-db-source.json
   ```

   If you installed the software correctly, you should see the service start and display the URL of the service: `http://localhost:3000`.

2. Make a test call to the service.

   ```
   curl <http://localhost:3000/users>
   ```

3. If the service is running correctly, you should see a list of users from the service, such as in this example.

   ```
   [
       {
           "last_name": "Smith",
           "first_name": "Ferdinand",
           "email": "f.smith@example.com",
           "id": 1
       },
       {
           "last_name": "Jones",
           "first_name": "Jill",
           "email": "j.jones@example.com",
           "id": 2
       },
       ...
   ```

You should see the list of users. If you receive an error in any step of the procedure, investigate, and correct the error before continuing. Some common situations that cause errors include:

1. You mistyped a command.
2. You aren't in the correct directory.
3. A required software component didn't install correctly.
4. A required software component isn't up to date.

If you see the list of users from the service, you're ready to do the [Tutorials](https://github.com/UWC2-APIDOC/to-do-service-sp25/blob/main/docs/tutorials.md).
