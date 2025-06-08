---
layout: default
title: PUT sightings
parent: Sightings resource
nav_order: 3
---

# `PUT /sightings` update a sighting

Updates the entire sightings record for the specified id. The request body must contain the complete updated sighting information, including any fields that remain unchanged.

* [Get sighting by id](./sightings-get.md)
* [Add a new sighting](./sightings-post.md)

## Method

`PUT`

## URL

`{base_url}/sightings/{id}`

Also see:

* [Base URL](../base-url.md)

## Headers

`Content-Type: application/json`

## Properties

You can use the following properties to update a sighting: `user_id`, `pod`, `time`, and `location`.

For a description of these properties, see [`/sightings` resource](./sightings-resource.md)

## Request body

Shows an example of some key-value pairs you could use to update an existing sighting.

⚠️  If you don't include the full data in your request, the server creates the sighting again with no data in that field. Likewise, if you don't include any data in your request, the server creates an empty sighting with the existing ID.

```json
{
    "user_id": 1,
    "pod": "unknown",
    "time": "2025-05-03T10:00",
    "location": "Lime Kiln Point State Park"
}
```

## Return body

Returns the information from the request body plus the ID specified in the URL.

```json
{
    "user_id": 1,
    "pod": "unknown",
    "time": "2025-05-03T10:00",
    "location": "Lime Kiln Point State Park",
    "id": 1
}
```

## Return status

| Status value | Return status | Description                                                  |
| ------------ | ------------- | ------------------------------------------------------------ |
| 200          | OK            | Request successful. The server has responded as required.    |
| 400          | Bad Request   | The server could not understand the request. Maybe a bad syntax? |

