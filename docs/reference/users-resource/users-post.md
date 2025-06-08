---
layout: default
title: POST users
parent: Users resource
nav_order: 2
---

# `POST /users`: add a new user

Creates a new user account for an orca whale watching enthusiast.

Also see:

* [Get user by id](./users-get.md)
* [Add a new sighting](../sightings-resource/sightings-post.md)

## Method

`POST`

## URL

`{base_url}/users/`

Also see:

* [Base URL](../base-url.md)

## Headers

`Content-Type: application/json`

## Properties

You can use the following properties to add a new user to the service: `first_name`, `last_name`, and `email`. The service automatically assigns the new user a unique `id`.

For a description of these properties, see [`/users` resource](./users-resource.md).

## Request body

This is an example of some key-value pairs you could use to update an existing user.

```json
{
    "last_name": "Waters",
    "first_name": "Ben",
    "email": "ben.waters@gmail.com"
}
```

⚠️  If you don't include any data in your request, the server creates an empty user with a unique ID.

## Return body

Returns the information from the request body.

```json
{
    "last_name": "Waters",
    "first_name": "Ben",
    "email": "ben.waters@gmail.com",
    "id": 6
}
```

## Return status

| Status value | Return status | Description                              |
| ------------ | ------------- | ---------------------------------------- |
| 201          | Created       | A new resource was created successfully. |

