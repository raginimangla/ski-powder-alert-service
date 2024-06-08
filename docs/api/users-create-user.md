---
layout: page
---

# Create a User

Register a new user profile with the Powder Alert service. This endpoint allows you to create a new user by providing the necessary details.
The request body contains the new user details.
You must specify the required properties for the user.

## URL

```shell

{POST}{server_url}/users/
```

## Request headers

This request does not use any authorization. The endpoint is available to all users and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data to be posted. | Optional | application/json. Default value.  |
| Accept | The format of the data to be returned. | Optional | application/json. Default value. |

## Request Body

In the request body, specify a JSON representation of the [`user`](user) object. The following table lists the properties that are required when you create a user.

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `last_name` | string | The user's last name. |
| `first_name` | string | The user's first name. |
| `email` | string | The user's email address. |
| `powder_threshold_inches` | integer | The users's preferred amount of fresh powder (in inches) for triggering alerts. When the amount of fresh powder at a resort meets or exceeds this value, an alert is triggered. |
| `id` | integer | The user's unique record ID. |

## Sample request

The POST body should look something like this. You can change the values of each property as you would like.

```js
[
    {
      "last_name": "Johnson",
      "first_name": "Larry",
      "email": "l.johnson@example.com",
      "powder_threshold_inches": 6
    }
]

```

## Response Body

The following example shows the response. Note that the names should be the same as you used in your **Request Body** and the response should include the new user’s ID. The user’s ID is automatically generated when the user is created.

```js
{
  "user_id": "123456",
  "last_name": "Johnson",
  "first_name": "Larry",
  "email": "l.johnson@example.com",
  "powder_threshold_inches": 6,
  "created_at": "2024-06-01T12:34:56Z"
}
```

## Return Status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 201 | Created | User data created successfully. |
| 500 | Internal server Error | Invalid JSON. |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
