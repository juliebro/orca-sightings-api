# `/sightings` resource

The `/sightings` resource lets you add a new orca whale sighting, update an existing sighting by its ID, list all sightings, list a sighting by its ID, or delete an existing sighting by its ID.

Also see the [`/users` resource](../users-resource/users-resource.md).

## Endpoint

`{base_url}/sightings`

Also see [Base URL](../base-url.md)

## Resource properties

This code block shows an example of a full `/sightings` resource:

```json
{
    "id": 1,
    "user_id": 1,
    "pod": "J-pod",
    "time": "2025-05-03T10:00",
    "location": "Lime Kiln Point State Park"
},
```

This table describes all of the fields available in the `/sightings` resource:

| Property   | Type      | Description                                                  | Example                        |
| ---------- | --------- | ------------------------------------------------------------ | ------------------------------ |
| `id`       | `integer` | Unique identifier for the sighting. Read-only and automatically generated. | `1`                            |
| `user_id`  | `integer` | The ID of the user who reported the sighting, as described in the [`/users` resource](../users-resource/users-resource.md). | `1`                            |
| `pod`      | `string`  | The identified pod of orca. Available attributes are `J-pod`, `K-pod`, `T49A`, and `unknown`). | `"J-pod"`                      |
| `time`     | `string`  | The timestamp of the sighting in [ISO 8601 format](../iso-8601-format.md).            | `"2025-05-03T10:00"`           |
| `location` | `string`  | The location where the sighting occurred.                    | `"Lime Kiln Point State Park"` |

## Actions by method

### `GET`

* [Get all sightings](./sightings-get.md)
* [Get a sighting by ID](./sightings-get.md)

### `POST`

* [Add a new sighting](./sightings-post.md)

### `PUT`

* [Update an existing sighting's information](./sightings-put.md)

### `PATCH`

* [Update part of an existing sighting's information](./sightings-patch.md)

### `DELETE`

* [Delete a sighting](./sightings-delete.md)
