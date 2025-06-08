---
layout: default
title: PUT users
parent: Users resource
nav_order: 3
---

# `PUT /users`: update a user

Updates the entire user record for the specified id. The request body must contain the complete updated user information, including any fields that remain unchanged.

* [Get user by id](./users-get.md)
* [Add a new user](./users-post.md)

## Method

`PUT`

## URL

`{base_url}/users/{id}`

Also see:
* [Base URL](../base-url.md)

## Headers

`Content-Type: application/json`

## Properties

| Property name | Type   | Description                                                  | Required? |
| ------------- | ------ | ------------------------------------------------------------ | --------- |
| `id`     | integer | The ID of the user you want to update. | Yes        |

## Request body

Shows an example of some key-value pairs you could use to update an existing user.

⚠️  If you don't include the full data in your request, the server creates the user again with no data in that field. Likewise, if you don't include any data in your request, the server creates an empty user with the same ID entered in the POST URL.

```
{
    "last_name": "Cartman",
    "first_name": "Eric M",
    "email": "eric.m.cartman@hotmail.com",
    "id": 3
}
```

## Return body

Returns the information from the request body.

```
{
    "last_name": "Cartman",
    "first_name": "Eric M",
    "email": "eric.m.cartman@hotmail.com",
    "id": 3
}
```

## Return status

| Status value | Return status | Description     |
| ------------ | ------------- | ----------------|
| 200          | OK       |  Request successful. The server has responded as required. |
| 400          | Bad Request | The server could not understand the request. Maybe a bad syntax? |
