---
layout: default
title: POST users
parent: Users resource
nav_order: 2
---

**On this page:**

- TOC
{:toc}

# `POST /users` add a new user

Creates a new user account for an orca whale watching enthusiast.

Also see:

- [Get user by id](./users-get.md)

## Method

`POST`

## URL

`{base_url}/users`

Also see:

- [Base URL](../base-url.md)

## Parameters

Optional, you should include all:  `first_name`, `last_name`, and `email`. The service automatically assigns the new user a unique `id`.

For a description of these properties, see [`/users` resource](./users-resource.md#parameters).

## Headers

`Content-Type: application/json`

## Request body

### cURL example

Shows creating a new user named Ben Waters.

```shell
curl -X POST \
     -H "Content-Type: application/json" \
     -d '{ "last_name": "Waters", "first_name": "Ben", "email": "ben.waters@gmail.com" }' \
     http://localhost:3000/users
```

### Postman example

Shows creating a new user named Ben Waters.

#### Request builder method and endpoint

Select **POST** and enter  `http://localhost:3000/users/`.

#### Request builder body

Select **Body > raw > JSON** and enter:

```json
{
  "last_name": "Waters",
  "first_name": "Ben",
  "email": "ben.waters@gmail.com"
}
```

## Response

Both of the previous examples return the information from the request body plus a unique ID.

```json
{
  "last_name": "Waters",
  "first_name": "Ben",
  "email": "ben.waters@gmail.com",
  "id": 5
}
```

## Postman return status

| Status value | Return status | Description                              |
| ------------ | ------------- | ---------------------------------------- |
| 201          | Created       | A new resource was created successfully. |
