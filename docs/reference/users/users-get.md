---
layout: default
title: GET users
parent: Users resource
nav_order: 1
---

- TOC
{:toc}

# `GET /users` list all users or a user by ID

Retrieves a list of all users or a user by ID.

## Method

`GET`

## URL

`{base_url}/users` - shows all existing users in the service

`{base_url}/users/{id}` - shows a specific user

## Parameters

Optional: the `id` of a particular user to list

For a description of all parameters, see [`/users` resource](./users-resource.md#parameters).

## Request body

### cURL example

Returns the user with an `id` of `4` .

```shell
curl -X GET http://localhost:3000/users/4
```

### Postman example

#### Request builder method and endpoint

Select **GET** and enter  `http://localhost:3000/users/4`.

#### Request builder body

None required.

## Response

Returns the full entry data for the specified user.

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
| 404          | Not Found     | Requested resource could not be found. |
