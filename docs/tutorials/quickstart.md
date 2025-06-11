---
layout: default
title: Get started by listing orca sightings
parent: Tutorials
nav_order: 2
---

# Get started by listing orca sightings: a tutorial

This tutorial shows you how to download the API files and try one of the service actions: viewing all of the orca sightings reported in the app for the San Juan Islands. If you already [set up your development environment](set-up-dev-env.md), the process should take about 15 minutes.

## Step 1: Make sure you have the API files

The files are located in the [orca-sightings-api repo on GitHub](https://github.com/juliebro/orca-sightings-api/tree/main/api). The directory contains the following files:

*  `orca-sightings-db.json`: a JSON file containing example users and sightings.
*  `orca-sightings.sh`: a shell script that starts JSON Server. Use this for Linux or macOS.
*  `orca-sightings.bat`: a batch file that starts JSON Server. Use this for Windows.

## Step 2: Start JSON Server

In a terminal window from the directory where you installed JSON Server, run:

```console
json-server -w orca-sightings-db.json
```

## Step 3: Use cURL or Postman to submit a request

```curl
cURL data here
```

*Postman info here*
