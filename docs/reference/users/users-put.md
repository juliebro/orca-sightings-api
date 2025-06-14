---
layout: default
title: PUT users
parent: Users resource
nav_order: 3
---

**On this page:**

- TOC
{:toc}

# `PUT /users` update a user

Updates the entire user record for the specified `id`.

- [Get user by id](./users-get.md)
- [Add a new user](./users-post.md)

## Method

`PUT`

## Endpoint

`{base_url}/users/{id}`

Also see:
- [Base URL](../base-url.md)

## Parameters

Required: The `id` of the user you want to update.

Optional, but all are recommended: You can specify these properties to replace an existing user: `first_name`, `last_name`, and `email`.

> If you don't include this data in your request, the server creates the user again with no data in that field. Likewise, if you don't include any data in your request, the server creates an empty user with the existing ID.

For a description of these properties, see [`/users` resource](./users-resource.md#parameters).

## Headers

`Content-Type: application/json`

## Request body

### cURL example

Shows replacing the user with an `id` of `4` with new data.

```shell
curl -X PUT \
     -H "Content-Type: application/json" \
     -d '{ "last_name": "Abernathy", "first_name": "Maura", "email": "maura.abernathy@gmail.com", "id": 4 }' \
     http://localhost:3000/users/3
```

### Postman example

Shows replacing the user with an `id` of `4`, as specified in the endpoint, with new data.

#### Request builder method and endpoint

Select **PUT** and enter  `http://localhost:3000/users/4`.

#### Request builder body

Select **Body > raw > JSON** and enter:

```json
{
  "last_name": "Abernathy",
  "first_name": "Maura",
  "email": "maura.abernathy@gmail.com",
}
```

## Return body

Returns the information from the request body, including the `id`:

```json
{
  "last_name": "Abernathy",
  "first_name": "Maura",
  "email": "maura.abernathy@gmail.com",
  "id": 4
}
```

## Postman return status

| Status value | Return status | Description     |
| ------------ | ------------- | ----------------|
| 200          | OK       |  Request successful. The server has responded as required. |
| 400          | Bad Request | The server could not understand the request. Maybe a bad syntax? |
