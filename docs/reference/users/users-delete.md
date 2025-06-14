---
layout: default
title: DELETE users
parent: Users resource
nav_order: 5
---

**On this page:**

- TOC
{:toc}

# `DELETE /users`: delete a user by ID

Deletes a user by ID.

Also see:

- [Get all users or a user by id](./users-get.md)

## Method

`DELETE`

## Endpoint

`{base_url}/users/{id}`

Also see:

- [Base URL](../base-url.md)

## Headers

`Content-Type: application/json`

## Parameters

Required: the `id` of the user you want to delete. Specify this in the endpoint.

For a full description of all `/users` properties, see [`/users` resource](./users-resource.md#parameters).

## Request body

### cURL example

Deletes the user with an `id` of `4` .

```shell
curl -X DELETE http://localhost:3000/users/4
```

### Postman example

#### Request builder method and endpoint

Select **DELETE** and enter  `http://localhost:3000/users/4`.

#### Request builder body

None required.

## Return body

Shows empty brackets.

```json
{}
```

{: .note }
If you don't specify a user ID, the service won't delete all the users. Instead, it returns a **404 Not Found** error message.

## Return status

| Status value | Return status | Description                                               |
| ------------ | ------------- | --------------------------------------------------------- |
| 200          | OK            | Request successful. The server has responded as required. |
| 404          | Not Found     | Requested resource could not be found.                    |
