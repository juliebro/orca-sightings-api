---
layout: default
title: Get started by listing orca sightings
parent: Tutorials
nav_order: 2
---

# Get started by listing orca sightings: a tutorial

This tutorial shows you how to download the API files and try one of the service actions: viewing all of the orca sightings reported in the app for the San Juan Islands. If you've already [set up your development environment](set-up-dev-env.md), the process should take about 15 minutes.

## Step 1: Make sure you have the API files

The files are located in the [orca-sightings-api repo on GitHub](https://github.com/juliebro/orca-sightings-api/tree/main/api). The directory contains the following files:

*  `orca-sightings-db.json`: a JSON file containing example users and sightings.
*  `orca-sightings.sh`: a shell script that starts JSON Server. Use this for Linux or macOS.
*  `orca-sightings.bat`: a batch file that starts JSON Server. Use this for Windows.

## Step 2: Start JSON Server with the Orca Sightings service

To start the Orca Sightings service:

1. Open a terminal window and `cd` to the location of the `json-server` application.

2. Make sure the API files are installed in the same directory. If they aren't copy or move them now.

3. Start the service by typing `json-server orca-sightings-db.json`. The service starts and lists some information to indicate it's running.

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

*Info here*

```json
Info to come
```

*Postman info here*
