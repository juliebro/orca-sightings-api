---
layout: default
title: DELETE sightings
parent: Sightings resource
nav_order: 5
---

**On this page:**

- TOC
{:toc}

# `DELETE /sightings` delete a sighting by ID

Deletes a sighting by its ID.

Also see:

- [Get all sightings or a sighting by ID](./sightings-get.md)

## Method

`DELETE`

## Endpoint

`{base_url}/sightings/{id}`

Also see:

- [Base URL](../base-url.md)

## Parameters

Required: The `id` of the user you want to delete. Specify this in the endpoint.

For a full description of all `/sightings` properties, see [`/sightings` resource](./sightings-resource.md#parameters).

## Request body

### cURL example

Shows deleting a sighting with an `id` of `4`.

```shell
curl -X DELETE \
  http://localhost:3000/sightings/4
```

### Postman example

#### Request builder method and endpoint

Select **DELETE** and enter  `http://localhost:3000/sightings/4`.

#### Request builder body

None required.

## Return body

Shows empty curly braces for both cURL and Postman.

```json
{}
```

> If you don't specify a sighting ID, the service won't delete all the sightings. Instead, the Postman app returns a `404 Not Found` error message.

## Return status

| Status value | Return status | Description                                               |
| ------------ | ------------- | --------------------------------------------------------- |
| 200          | OK            | Request successful. The server has responded as required. |
| 404          | Not Found     | Requested resource could not be found.                    |
