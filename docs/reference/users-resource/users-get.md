---
layout: default
title: GET users
parent: Users resource
nav_order: 1
---

- TOC
{:toc}

# `GET /users`: show all users or a user by ID

Retrieves a list of all users or a user by ID.

## Method

`GET`

## URL

`{base_url}/users`  - shows all existing users in the service

`{base_url}/users/{id}` - shows a specific user

## Properties

`id` - the ID of a particular user to show

For a description of all properties, see [`/users` resource](./users-resource.md).

## Request body

None.

## Return body

Returns all users or the specific user requested.

## Examples

Retrieve all users with cURL:

```shell
curl -X GET http://localhost:3000/users
```

Response:

``json
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

Retrieve the user with an `id` of `4` with cURL:

```shell
curl -X GET http://localhost:3000/users/4
```

Response:

```json
{
    "last_name": "Cartman",
    "first_name": "Eric M",
    "email": "eric.m.cartman@hotmail.com",
    "id": 4
}
```

## Return status

| Status value | Return status | Description                                               |
| ------------ | ------------- | --------------------------------------------------------- |
| 200          | OK            | Request successful. The server has responded as required. |
| 404          | Not Found     | Requested resource could not be found.                    |
