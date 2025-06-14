---
layout: default
title: Add a new user
parent: Tutorials
nav_order: 4
---

**On this page:**

- TOC
{:toc}

# Add a new user to the Orca Sightings service: a tutorial

{: .comment }
This page is in progress.

This tutorial should take you about 15 minutes to complete.

Also see the API reference pages:

- [PUT /users](../reference/users-resource/users-put.md)
- [PATCH /users](../reference/users-resource/users-patch.md)

## Before you begin

Make sure you've [set up your development environment](./set-up-dev-env.md).

## Step 1: Start the Orca Sightings service

1. Open a terminal window and cd to the location of `json-server`.

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

## Step 2: Open Postman

> Info to come.
