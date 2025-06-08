---
layout: default
title: DELETE sightings
parent: Sightings resource
nav_order: 5
---

# `DELETE /sightings` delete a sighting by ID

Delete a sighting by its ID.

Also see:

* [Get all sightings or a sighting by ID](./sightings-get.md)

## Method

`DELETE`

## URL

`{base_url}/sightings/{id}`

## Properties

None.

## Headers

`Content-Type: application/json`

## Request body

None.

## Return body

Deletes the sighting specified.

📒 If you don't specify a sighting ID, all the sightings won't be deleted. Instead, the service returns a 404 Not Found error message. 

```json
{}
```

## Return status

| Status value | Return status | Description                                               |
| ------------ | ------------- | --------------------------------------------------------- |
| 200          | OK            | Request successful. The server has responded as required. |
| 404          | Not Found     | Requested resource could not be found.                    |

