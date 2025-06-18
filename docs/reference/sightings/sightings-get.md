---
layout: default
title: GET sightings
parent: Sightings resource
nav_order: 1
---

**On this page:**

- TOC
{:toc}

# `GET /sightings` list all sightings or a sighting by ID

Lists all sightings of orca whales reported in the service or a sighting by ID.

Also see:

- [Add a sighting](./sightings-post.md)

## Method

`GET`

## Endpoints

`{base_url}/sightings`: lists all existing sightings in the service

`{base_url}/sightings/{id}`: lists a specific sighting

Also see:

- [Base URL](../base-url.md)

## Properties

Optional: the `id` of a specific sighting to list.

For a full description of all `/sightings` properties, see [`/sightings` resource](./sightings-resource.md#properties).

## Headers

`Content-Type: application/json`

## Request body

### cURL example

Returns the sighting with an `id` of `2` .

```shell
curl -X GET http://localhost:3000/sightings/2
```

### Postman example

#### Request builder method and endpoint

Select **GET** and enter  `http://localhost:3000/sightings/2`.

#### Request builder body

None required.

## Return body

Returns all sightings or the specific sighting requested. The following example shows the result of requesting the sighting with an `id` of `2`.

```json
{
  "id": 2,
  "user_id": 3,
  "pod": "T49A",
  "time": "2025-05-01T19:00",
  "location": "Patos Island"
}
```

## Postman return status

| Status value | Return status | Description                                               |
| ------------ | ------------- | --------------------------------------------------------- |
| 200          | OK            | Request successful. The server has responded as required. |
| 404          | Not Found     | Requested resource could not be found.                    |
