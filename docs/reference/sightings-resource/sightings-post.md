---
layout: default
title: POST sightings
parent: Sightings resource
nav_order: 2
---

- TOC
{:toc}

# `POST /sightings`: add a new sighting

Creates a new orca whale sighting.

Also see:

* [Get sighting by id](./sightings-get.md)

## Method

`POST`

## URL

`{base_url}/sightings`

Also see:

* [Base URL](../base-url.md)

## Headers

`Content-Type: application/json`

## Properties

You can use the following properties to add a new sighting to the service: `user_id`, `pod`, `time`, and `location`. The service automatically assigns the new user a unique `id`.

For a description of these properties, see [`/sightings` resource](./sightings-resource.md).

## Request body

This is an example of some key-value pairs you could use to add a sighting.

```json
{
    "user_id": 1,
    "pod": "K-pod",
    "time": "2024-12-24T09:20",
    "location": "Friday Harbor"
}
```

⚠️  If you don't include any data in your request, the server creates an empty sighting with a unique ID.

## Return body

Returns the information from the request body plus a unique ID.

```json
{
    "user_id": 1,
    "pod": "K-pod",
    "time": "2024-12-24T09:20",
    "location": "Friday Harbor",
    "id": 9
}
```

## Return status

| Status value | Return status | Description                              |
| ------------ | ------------- | ---------------------------------------- |
| 201          | Created       | A new resource was created successfully. |

