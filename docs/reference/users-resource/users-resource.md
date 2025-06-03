# `/users` resource

The `/users` resource lets you add a new user, update an existing user, list all users, list a user by its ID, or delete an existing user by its ID.

Also see [`/sightings` resource](../sightings-resource/sightings-resource.md).

## Endpoint

`{base_url}/users`

Also see [Base URL](../base-url.md).

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

| Property     | Type      | Description                                                  | Example                  |
| ------------ | --------- | ------------------------------------------------------------ | ------------------------ |
| `last_name`  | `string`  | The user's last name.                                        | `"Marsh"`                |
| `first_name` | `string`  | The user's first name.                                       | `"Stan"`                 |
| `email`      | `string`  | The user's email address. Must be unique.                    | `"stan.marsh@gmail.com"` |
| `id`         | `integer` | Unique identifier for the user. Read-only, automatically generated. | `1`               |

## Actions by method

### `GET`

* [Get all users](./users-get.md)
* [Get an existing user by ID](./users-get.md)

### `POST`

* [Create a new user](./users-post.md)

### `PUT`

* [Update an existing user's information](./users-put.md)

### `DELETE`

* [Delete a user by ID](./users-delete.md)
