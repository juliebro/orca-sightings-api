---
layout: default
title: PUT users
parent: Users resource
nav_order: 3
---

- TOC
{:toc}

# `PUT /users`: update a user

Updates the entire user record for the specified id. The request body must contain the complete updated user information, including any fields that remain unchanged.

- [Get user by id](./users-get.md)
- [Add a new user](./users-post.md)

## Method

`PUT`

## URL

`{base_url}/users/{id}`

Also see:
- [Base URL](../base-url.md)

## Headers

`Content-Type: application/json`

## Properties

In the endpoint URL, include the `id` of the user you want to update.

You must specify these properties to replace an existing user: `first_name`, `last_name`, and `email`.

> If you don't include this data in your request, the server creates the user again with no data in that field. Likewise, if you don't include any data in your request, the server creates an empty user with the existing ID.

For a description of these properties, see [`/users` resource](./users-resource.md).

# Examples

Replace user with an `id` of `4` with new data:

```shell
curl -X PUT \
     -H "Content-Type: application/json" \
     -d '{ "last_name": "Abernathy", "first_name": "Maura", "email": "maura.abernathy@gmail.com", "id": 4 }' \
     http://localhost:3000/users/3
```

Postman request body:

```json
{
  "last_name": "Abernathy",
  "first_name": "Maura",
  "email": "maura.abernathy@gmail.com",
}
```

Returns the information from the request body, including the `id`:

```json
{
  "last_name": "Abernathy",
  "first_name": "Maura",
  "email": "maura.abernathy@gmail.com",
  "id": 4
}
```

## Return status

| Status value | Return status | Description     |
| ------------ | ------------- | ----------------|
| 200          | OK       |  Request successful. The server has responded as required. |
| 400          | Bad Request | The server could not understand the request. Maybe a bad syntax? |
