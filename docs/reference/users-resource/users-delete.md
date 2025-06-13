---
layout: default
title: DELETE users
parent: Users resource
nav_order: 5
---

- TOC
{:toc}

# `DELETE /users`: delete a user by ID

Delete a user by ID.

Also see:

- [Get all users or a user by id](./users-get.md)

## Method

`DELETE`

## URL

`{base_url}/users/{id}` - deletes a specific user

## Properties

None.

## Headers

`Content-Type: application/json`

## Request body

None.

## Return body

Deletes the user specified.

> If you don't specify a user ID, all the users won't be deleted. Instead, the service returns a 404 Not Found error message.

```json
{}
```

## Return status

| Status value | Return status | Description                                               |
| ------------ | ------------- | --------------------------------------------------------- |
| 200          | OK            | Request successful. The server has responded as required. |
| 404          | Not Found     | Requested resource could not be found.                    |

