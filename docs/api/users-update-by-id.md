---
layout: page
---

# Update a User By ID

Update details of a specific user using their unique ID. This endpoint allows you to modify user information such as their last name, first name, email, and powder threshold.

## URL

```shell

{PATCH}{server_url}/users/{user_id}
```

## Request headers

This request does not use any authorization. The endpoint is available to all users and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data to be posted. | Optional | application/json. Default value.  |
| Accept | The format of the data to be returned. | Optional | application/json. Default value. |

## Request Body

In the request body, specify a JSON representation of the [`user`](user) object. The following table lists the properties that are required when you udpate a user.

| Property name           | Type     | Description                                              |
|-------------------------|----------|----------------------------------------------------------|
| last_name               | String   | The last name of the user.                               |
| first_name              | String   | The first name of the user.                              |
| email                   | String   | The email address of the user.                           |
| powder_threshold_inches | Integer  | The snowfall threshold in inches for the user to receive alerts. |

## Sample request

The PATCH request should look something like this. Replace `{server_url}` and `{user_id}`with the actual server URL and the user ID, and include the request body with the details of the user to be updated.

```js
{
      "last_name": "Updated Last Name",
      "first_name": "Updated First Name",
      "email": "updated_email@example.com",
      "powder_threshold_inches": 8
    }'
```

## Response Body

The response will include the updated resort details.

```js
{
    "user_id": 1,
    "resort_name": "Hill Country",
    "location": "Texas",
    "fresh_powder_inches": 12,
    "traffic_conditions": "Medium",
    "id": 1234
}

```

## Return Status

| Status value    | Return status         | Description                                    |
|-----------------|-----------------------|------------------------------------------------|
| 200             | OK                    | Resort was successfully updated.               |
| 400             | Bad Request           | The request was invalid or missing parameters. |
| 404             | Not Found             | The resort with the specified ID was not found. |
| 500             | Internal Server Error | An error occurred on the server.               |
| ECONNREFUSED    | N/A                   | Service is offline. Start the service and try again. |

## Related information
