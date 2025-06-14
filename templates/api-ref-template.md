---
layout: default
nav_order: 3
---

# `POST /sightings` add a sighting

Adds a new sighting.

Before you add a sighting, you should have a user to assign it to.

- [Get user by id](https://github.com/UWC2-APIDOC/to-do-service-sp25/blob/main/docs/api/users-get-user-by-id.md)
- [Add a new user](https://github.com/UWC2-APIDOC/to-do-service-sp25/blob/main/docs/tutorials/enroll-a-new-user.md)

## Method

`POST`

## Endpoint

`{base_url}/sightings`

## Parameters

| Parameter name | Type   | Description                                                  | Required? |
| ------------- | ------ | ------------------------------------------------------------ | --------- |
| `user_id`     | number | The ID of the assigned user                                  | No        |
| `title`       | string | The title or short description of the task                   | No        |
| `description` | string | A more specific description of the task                      | No        |
| `due_date`    | string | The [date and time](https://en.wikipedia.org/wiki/ISO_8601) the task is due | No        |
| `warning`     | number | The number of minutes relative to the `due_date` to alert the user of the task. This is normally a negative number to alert the user before the `due_date`. | No        |

You should specify at least a `user_id` and a `title`, even though the Orca Sightings service doesn't require any properties.

## Headers

```
Content-Type: application/json
```

## Request body

Shows an example of some key-value pairs you could use to create a new task.

```
{
    "user_id": 23,
    "title": "Set up Zoom meeting with web team",
    "description": "Kick off new product release campaign",
    "due_date": "2025-05-26T14:00",
    "warning": "-10"
}
```

## Return body

Returns the information from the request body plus a unique ID for the task.

```
{
    "user_id": 23,
    "title": "Set up Zoom meeting with web team",
    "description": "Kick off new product release campaign",
    "due_date": "2025-05-19T14:00",
    "warning": "-10",
    "id": 5
}
```

## Return status

| Status value | Return status | Description                                                  |
| ------------ | ------------- | ------------------------------------------------------------ |
| 201          | Created       | The server successfully created a new resource.              |
| 400          | Bad Request   | The server couldn't understand the request. Maybe a bad syntax? |
