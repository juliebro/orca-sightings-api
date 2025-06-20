---
layout: default
title: PATCH users
parent: Users resource
nav_order: 4
---

**On this page:**

- TOC
{:toc}

# `PATCH /users`: Update some of the details about a user

Updates some of the details about a user.

Also see:

- [Update all or part of a user entry: a tutorial](../../tutorials/update-user.md)
- [GET: List all users](./users-get.md)
- [GET: Get user by id](./users-get.md)
- [PATCH: Update part of a sighting](../sightings/sightings-patch.md)

## Method

`PATCH`

## Endpoint

`{base_url}/users/{id}`

Also see:

- [Base URL](../base-url.md)

## Properties

Required: the `id` of the user you want to update.

For a description of all properties, see [`/users` resource](./users-resource.md#properties).

## Headers

`Content-Type: application/json`

## Request body

### cURL example

Shows updating the `first_name` of the user with an `id` of `1`.

```shell
curl -X PATCH \
  -H "Content-Type: application/json" \
  -d '{
    "first_name": "Benjamin"
  }' \
  http://localhost:3000/users/6
```

### Postman example

Shows updating the `first_name` of the user with an `id` of `6`.

#### Request builder method and endpoint

Select **PATCH** and enter  `http://localhost:3000/users/6`.

#### Request builder body

Select **Body > raw > JSON** and enter:

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
