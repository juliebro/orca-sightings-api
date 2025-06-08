---
layout: default
title: PATCH sightings
parent: Sightings resource
nav_order: 4
---

# `PATCH /sightings`: update part of an existing sighting

Updates some of the details about a sighting.

Also see:

* [List all sightings](./sightings-get.md)
* [Get sighting by id](./sightings-get.md)

## Method

`PATCH`

## URL

`{base_url}/sightings/{id}`

## Properties

You can use the following properties to update part of a sighting: `user_id`, `pod`, `time`, and `location`.

For a description of these properties, see [`/sightings` resource](./sightings-resource.md).

## Headers

`Content-Type: application/json`

## Request body

Shows an example of some key-value pairs you could use to update some data for a user.

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

## Return status

| Status value | Return status | Description                                               |
| ------------ | ------------- | --------------------------------------------------------- |
| 200          | OK            | Request successful. The server has responded as required. |
| 404          | Not Found     | Requested resource could not be found.                    |

