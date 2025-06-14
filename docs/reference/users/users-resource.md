---
layout: default
title: Users resource
parent: API reference
nav_order: 1
has_toc: false
---

**On this page:**

- TOC
{:toc}

# `/users` resource

The `/users` resource lets you add a new user, update all or part of an existing user, list all users, list a user by its ID, or delete an existing user by its ID. Users represent the whale watching enthusiasts who report orca sightings.

Also see [`/sightings` resource](../sightings/sightings-resource.md).

## Endpoint

`{base_url}/users`

Also see [Base URL](../base-url.md).

## Parameters

Shows an example of a full `/users` resource:

```json
{
    "last_name": "Marsh",
    "first_name": "Stan",
    "email": "stan.marsh@gmail.com",
    "id": 1
}
```

Describes all parameters available in the `/users` resource:

| Parameter     | Type      | Description                                                  | Example                  |
| ------------ | --------- | ------------------------------------------------------------ | ------------------------ |
| `last_name`  | `string`  | The user's last name.                                        | `"Marsh"`                |
| `first_name` | `string`  | The user's first name.                                       | `"Stan"`                 |
| `email`      | `string`  | The user's email address. Must be unique.                    | `"stan.marsh@gmail.com"` |
| `id`         | `integer` | Unique identifier for the user. Read-only, automatically generated. | `1`               |

## Actions by method

### `GET`

- [Get all users](./users-get.md)
- [Get an existing user by ID](./users-get.md)

### `POST`

- [Create a new user](./users-post.md)

### `PUT`

- [Update an existing user's information](./users-put.md)

### `PATCH`

- [Update part of an existing user's information](./users-patch.md)

### `DELETE`

- [Delete a user by ID](./users-delete.md)
