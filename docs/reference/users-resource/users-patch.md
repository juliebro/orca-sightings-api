---
layout: default
title: PATCH users
parent: Users resource
nav_order: 4
---

# `PATCH /users`: Update some of the details about a user

Updates some of the details about a user.

Also see:

* [Update all or part of a user entry: a tutorial](../../tutorials/update-user.md)
* [GET: List all users](./users-get.md)
* [GET: Get user by id](./users-get.md)
* [PATCH: Update part of a sighting](../sightings-resource/sightings-patch.md)

## Method

`PATCH`

## URL

`{base_url}/users/{id}`

## Properties

`id` - the ID of the user to be updated

For a description of all properties, see [`/users` resource](./users-resource.md).

## Headers

`Content-Type: application/json`

## Request body

Shows an example of some key-value pairs you could use to update some data for a user.

```json
{
    "first_name": "Benjamin"
}
```

## Return body

Returns the updated user entry.

```json
{
    "last_name": "Waters",
    "first_name": "Benjamin",
    "email": "ben.waters@gmail.com",
    "id": 6
}
```

## Return status

| Status value | Return status | Description                                               |
| ------------ | ------------- | --------------------------------------------------------- |
| 200          | OK            | Request successful. The server has responded as required. |
| 404          | Not Found     | Requested resource could not be found.                    |

