---
layout: default
title: POST users
parent: Users resource
nav_order: 2
---

- TOC
{:toc}

# `POST /users`: add a new user

Creates a new user account for an orca whale watching enthusiast.

Also see:

- [Get user by id](./users-get.md)

## Method

`POST`

## URL

`{base_url}/users`

Also see:

* [Base URL](../base-url.md)

## Headers

`Content-Type: application/json`

## Properties

You can use the following properties to add a new user to the service: `first_name`, `last_name`, and `email`. The service automatically assigns the new user a unique `id`.

For a description of these properties, see [`/users` resource](./users-resource.md).

## Examples

Use cURL to create a new user named Ben Waters:

```shell
curl -X POST \
     -H "Content-Type: application/json" \
     -d '{ "last_name": "Waters", "first_name": "Ben", "email": "ben.waters@gmail.com" }' \
     http://localhost:3000/users
```

In Postman, you'd add the following text in the body:

```json
{
  "last_name": "Waters",
  "first_name": "Ben",
  "email": "ben.waters@gmail.com"
}
```

Both of the previous examples return the information from the request body plus a unique ID.

```json
{
  "last_name": "Waters",
  "first_name": "Ben",
  "email": "ben.waters@gmail.com",
  "id": 5
}
```

> If you don't include any data in your request, the server creates an empty sighting with a unique ID.

## Postman return status

| Status value | Return status | Description                              |
| ------------ | ------------- | ---------------------------------------- |
| 201          | Created       | A new resource was created successfully. |
