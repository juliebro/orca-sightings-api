---
layout: default
title: PUT sightings
parent: Sightings resource
nav_order: 3
---

- TOC
{:toc}

# `PUT /sightings` update a sighting

Updates the entire sightings record for the specified `id`. The request body must contain the complete updated sighting information, including any fields that remain unchanged.

- [Get sighting by id](./sightings-get.md)
- [Add a new sighting](./sightings-post.md)

## Method

`PUT`

## Endpoint

`{base_url}/sightings/{id}`

Also see:

* [Base URL](../base-url.md)

## Parameters

Required: specify the `id` of the sighting you want to update in the endpoint.

Optional, but all are recommended: you can use the following parameters to update a sighting: `user_id`, `pod`, `time`, and `location`. 

> If you don't include the full data in your request, the server creates the sighting again with no data in that field. Likewise, if you don't include any data in your request, the server creates an empty sighting with the existing ID.

For a description of these parameters, see [`/sightings` resource](./sightings-resource.md#parameters).

## Headers

`Content-Type: application/json`

## Request body

### cURL example

Shows updating the information for the user with an `id` of `1`.

```shell
curl -X PUT \
  -H "Content-Type: application/json" \
  -d '{
    "user_id": 1,
    "pod": "K-pod",
    "time": "2025-05-03T10:30",
    "location": "Lime Kiln Point State Park"
  }' \
  http://localhost:3000/sightings/1
```

### Postman example

Shows updating the information for the user with an `id` of `1`, as specified in the endpoint.

#### Request builder method and endpoint

Select **PUT** and enter `http://localhost:3000/sightings/1`.

#### Request builder body

Select **Body > raw > JSON** and enter:

```json
{
  "user_id": 1,
  "pod": "K-pod",
  "time": "2025-05-03T10:30",
  "location": "Lime Kiln Point State Park"
}
```

## Response

Returns the information from the request body plus the ID specified in the endpoint.

```json
{
  "user_id": 1,
  "pod": "unknown",
  "time": "2025-05-03T10:00",
  "location": "Lime Kiln Point State Park",
  "id": 1
}
```

## Postman return status

| Status value | Return status | Description                                                  |
| ------------ | ------------- | ------------------------------------------------------------ |
| 200          | OK            | Request successful. The server has responded as required.    |
| 400          | Bad Request   | The server could not understand the request. Maybe a bad syntax? |
