---
layout: default
title: POST sightings
parent: Sightings resource
nav_order: 2
---

**On this page:**

- TOC
{:toc}

# `POST /sightings` add a new sighting

Creates a new orca whale sighting. Before you add a sighting, you should have a user to assign it to.

Also see:

- [Add a new user](../users/add-user.md)
- [Get sighting by id](./sightings-get.md)

## Method

`POST`

## Endpoint

`{base_url}/sightings`

Also see:

- [Base URL](../base-url.md)

## Properties

Optional, but recommended: `user_id`, `pod`, `time`, and `location`. The service automatically assigns the new user a unique `id`.

> If you don't include any data in your request, the server creates an empty sighting with a unique ID.

For a description of these properties, see [`/sightings` resource](./sightings-resource.md#properties).

## Headers

`Content-Type: application/json`

## Request body

### cURL example

Shows an example of adding a new sighting using all available parameters.

```shell
curl -X POST \
     -H "Content-Type: application/json" \
     -d '{ "user_id": 1, "pod": "K-pod", "time": "2024-12-24T09:20", "location": "Friday Harbor" }' \
     http://localhost:3000/sightings
```

### Postman example

Shows an example of adding a new sighting using all available parameters.

```json
{
  "user_id": 1,
  "pod": "K-pod",
  "time": "2024-12-24T09:20",
  "location": "Friday Harbor"
}
```

## Response

Shows the response for the previous request body examples.

```json
{
  "user_id": 1,
  "pod": "K-pod",
  "time": "2024-12-24T09:20",
  "location": "Friday Harbor",
  "id": 9
}
```

## Postman return status

| Status value | Return status | Description                              |
| ------------ | ------------- | ---------------------------------------- |
| 201          | Created       | A new resource was created successfully. |
