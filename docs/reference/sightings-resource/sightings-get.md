---
layout: default
title: GET sightings
parent: Sightings resource
nav_order: 1
---

# `GET /sightings`: list all sightings or a sighting by ID

Lists all sightings of orca whales reported in the service or a sighting by ID.

Also see:

* [Add a sighting](./sightings-post.md)

## Method

`GET`

## URL

`{base_url}/sightings`  - shows all existing sightings in the service

`{base_url}/sightings/{id}` - shows a specific sighting

## Properties

`id` - the ID of a particular sighting to show

For a description of all sightings, see [`/sightings` resource](./sightings-resource.md).

## Headers

`Content-Type: application/json`

## Request body

None.

## Return body

Returns all sightings or the specific sighting requested. The following example shows the result of requesting all sightings.

```json
[
    {
        "id": 1,
        "user_id": 1,
        "pod": "J-pod",
        "time": "2025-05-03T10:00",
        "location": "Lime Kiln Point State Park"
    },
    {
        "id": 2,
        "user_id": 3,
        "pod": "T49A",
        "time": "2025-05-01T19:00",
        "location": "Patos Island"
    },
    {
        "id": 3,
        "user_id": 4,
        "pod": "unknown",
        "time": "2025-04-28T12:30",
        "location": "Shaw Island"
    },
    {
        "id": 4,
        "user_id": 3,
        "pod": "K-pod",
        "time": "2025-02-15T10:00",
        "location": "Lime Kiln Point State Park"
    },
    {
        "id": 5,
        "user_id": 2,
        "pod": "J-pod",
        "time": "2025-01-20T13:00",
        "location": "Lime Kiln Point State Park"
    },
    {
        "id": 6,
        "user_id": 1,
        "pod": "K-pod",
        "time": "2024-12-24T17:15",
        "location": "Friday Harbor"
    },
    {
        "id": 7,
        "user_id": 4,
        "pod": "T49A",
        "time": "2025-12-13T06:00",
        "location": "Reuben Tarte County Park"
    },
    {
        "id": 8,
        "user_id": 2,
        "pod": "T49A",
        "time": "2025-01-30T11:00",
        "location": "Lime Kiln Point State Park"
    }
]
```

## Return status

| Status value | Return status | Description                                               |
| ------------ | ------------- | --------------------------------------------------------- |
| 200          | OK            | Request successful. The server has responded as required. |
| 404          | Not Found     | Requested resource could not be found.                    |

