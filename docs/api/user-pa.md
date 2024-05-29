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

* [Get all users](users-get-all-users)
* [Get users by ID](users-get-user-by-id)
* [Get users by email](users-get-user-by-email)
* [Get users by first name](users-get-users-first-name)
* [Get users by last name](users-get-users-last-name)
* [Get users by powder threshold](users-get-users-powder-threshold)

### CREATE (POST)

* [Create user](users-create-user)

### UPDATE (PUT/PATCH)

* [Update user by ID](users-update-by-id)
* [Change user email](users-change-user-email.md)
* [Change user property](users-change-user-property)

### DELETE

* [Delete user by ID](users-delete-user-by-id)
