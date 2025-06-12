---
layout: default
title: GET users
parent: Users resource
nav_order: 1
---

- TOC
{:toc}

# `GET /users`: show all users or a user by ID

Lists all users or a user by ID.

Also see:

* *Info to come*

## Method

`GET`

## URL

`{base_url}/users`  - shows all existing users in the service

`{base_url}/users/{id}` - shows a specific user

## Properties

`id` - the ID of a particular user to show

For a description of all properties, see [`/users` resource](./users-resource.md).

## Headers

`Content-Type: application/json`

## Request body

None.

## Return body

Returns all users or the specific user requested. The following example shows the result of requesting all users.

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
        "last_name": "McCormick",
        "first_name": "Kenny",
        "email": "kenny.mccormick@gmail.com",
        "id": 3
    },
    {
        "last_name": "Cartman",
        "first_name": "Eric M",
        "email": "eric.m.cartman@hotmail.com",
        "id": 4
    }
]
```

## Return status

| Status value | Return status | Description                                               |
| ------------ | ------------- | --------------------------------------------------------- |
| 200          | OK            | Request successful. The server has responded as required. |
| 404          | Not Found     | Requested resource could not be found.                    |

