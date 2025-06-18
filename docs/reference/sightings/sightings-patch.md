---
layout: default
title: PATCH sightings
parent: Sightings resource
nav_order: 4
---

**On this page:**

- TOC
{:toc}

# `PATCH /sightings` update part of an existing sighting

Updates some of the details about a sighting.

Also see:

- [List all sightings](./sightings-get.md)
- [Get sighting by id](./sightings-get.md)

## Method

`PATCH`

## Endpoint

`{base_url}/sightings/{id}`

## Properties

Required: specify a sighting `id`.

Optional, but you should include at least one: `user_id`, `pod`, `time`, and `location`.

For a description of these properties, see [`/sightings` resource](./sightings-resource.md#properties).

## Headers

`Content-Type: application/json`

## Request body

### cURL example

Shows updating the time for the sighting with an `id` of `1`.

```shell
curl -X PATCH \
  -H "Content-Type: application/json" \
  -d '{
    "time": "2025-05-03T11:00"
  }' \
  http://localhost:3000/sightings/1
```

### Postman example

Shows an example of a key-value pair you could use to update some data for a user.

```json
{
  "time": "2025-05-03T11:00",
}
```

## Return body

Returns the updated sightings entry.

```json
{
  "user_id": 1,
  "pod": "unknown",
  "time": "2025-05-03T11:00",
  "location": "Lime Kiln Point State Park",
  "id": 1
}
```

## Postman return status

| Status value | Return status | Description                                               |
| ------------ | ------------- | --------------------------------------------------------- |
| 200          | OK            | Request successful. The server has responded as required. |
| 404          | Not Found     | Requested resource could not be found.                    |
