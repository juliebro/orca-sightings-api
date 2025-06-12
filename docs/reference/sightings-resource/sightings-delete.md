---
layout: default
title: DELETE sightings
parent: Sightings resource
nav_order: 5
---

- TOC
{:toc}

# `DELETE /sightings` delete a sighting by ID

Delete a sighting by its ID.

Also see:

- [Get all sightings or a sighting by ID](./sightings-get.md)

## Method

`DELETE`

## URL

`{base_url}/sightings/{id}`

Also see:

- [Base URL](../base-url.md)

## Properties

The endpoint requires `id`, which is the unique id of the user you want to delete.


## Headers

`Content-Type: application/json`

## Request body

None.

## Return body

Deletes the sighting specified.

> If you don't specify a sighting ID, the service won't delete all the sightings. Instead, the it returns a `404 Not Found` error message.

```json
{}
```

## Return status

| Status value | Return status | Description                                               |
| ------------ | ------------- | --------------------------------------------------------- |
| 200          | OK            | Request successful. The server has responded as required. |
| 404          | Not Found     | Requested resource could not be found.                    |
