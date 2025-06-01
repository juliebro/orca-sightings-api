# `/users` resource

The `/users` resource does (info to come).

Also see:

* *Info to come.*

## Resource properties

This code block shows an example of a full `/users` resource:

```json
{
    "last_name": "Marsh",
    "first_name": "Stan",
    "email": "stan.marsh@gmail.com",
    "id": 1
},
```

This table describes all of the fields available in the `/users` resource:

| Field        | Type      | Description                                                  | Example                  |
| ------------ | --------- | ------------------------------------------------------------ | ------------------------ |
| `last_name`  | `string`  | The user's last name.                                        | `"Marsh"`                |
| `first_name` | `string`  | The user's first name.                                       | `"Stan"`                 |
| `email`      | `string`  | The user's email address. Must be unique.                    | `"stan.marsh@gmail.com"` |
| `id`         | `integer` | Unique identifier for the user. Read-only, automatically generated. | `1`                      |

## Actions by method

*(This section will link to the relevant reference topics.)*

### `GET`

* Get all sightings
* Get a sighting by ID

### `POST`

* Create a new sighting

### `PUT`

* Update an existing sighting's information

### `DELETE`

* Delete a sighting
