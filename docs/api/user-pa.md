---
layout: page
---
# `user` resource

Base endpoint:

```shell
{server_url}/users
```

Contains information about the users of the service.

## Resource properties

Sample `user` resource

```js
{
      "last_name": "Johnson",
      "first_name": "Larry",
      "email": "l.johnson@example.com",
      "powder_threshold_inches": 6,
      "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `last_name` | string | The user's last name. |
| `first_name` | string | The user's first name. |
| `email` | string | The user's email address. |
| `powder_threshold_inches` | integer | The amount of fresh powder in inches for triggering alerts. When the amount of fresh powder at a resort meets or exceeds this value, an alert is triggered. |
| `id` | integer | The user's unique record ID. |

## Operations

The `user` resource supports these operations.

### READ (GET)

* [Get all users](docs/api/users-get-all-users.md)
* [Get users by ID](docs/api/users-get-user-by-id.md)
* [Get users by powder threshold](docs/api/users-get-users-by-threshold.md)

### CREATE (POST)

* [Create user](docs/api/users-create-user.md)

### UPDATE (PUT/PATCH)

* [Update user by ID](/docs/api/users-update-by-id.md)
