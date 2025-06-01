# `/sightings` resource

The `/sightings` resource does *(info to come)*.

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

| Field      | Type      | Description                                                  | Example                        |
| ---------- | --------- | ------------------------------------------------------------ | ------------------------------ |
| `id`       | `integer` | Unique identifier for the sighting. Read-only and automatically generated. | `1`                            |
| `user_id`  | `integer` | The ID of the user who reported the sighting, as described in the [`/users` resource](https://github.com/juliebro/orca-sightings-api/blob/7f3d2c8d3508db2629cea03135e8c147651aa91f/docs/reference/users-resource). | `1`                            |
| `pod`      | `string`  | The identified pod of orca. Available attributes are `J-pod`, `K-pod`, `T49A`, and `unknown`). | `"J-pod"`                      |
| `time`     | `string`  | The timestamp of the sighting in ISO 8601 format.            | `"2025-05-03T10:00"`           |
| `location` | `string`  | The location where the sighting occurred.                    | `"Lime Kiln Point State Park"` |

## Actions by method

*(This section will link to the relevant reference topics.)*

### `GET`

- Get all users
- Get user by ID

### `POST`

- Create a user

### `PUT`

- Update an existing user's information

### `DELETE`

- Delete a user
