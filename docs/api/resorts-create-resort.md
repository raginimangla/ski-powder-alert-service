---
layout: page
---

# Add a Resort

Register a new resort with the Powder Alert service. This endpoint allows you to create a new resort with details such as the resort name, location, current fresh powder inches, and traffic conditions.
The request body contains the new user details.
You must specify the required properties for the user.

## URL

```shell

{POST}{server_url}/resorts/
```

## Request headers

This request does not use any authorization. The endpoint is available to all users and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data to be posted. | Optional | application/json. Default value.  |
| Accept | The format of the data to be returned. | Optional | application/json. Default value. |

## Request Body

In the request body, specify a JSON representation of the [`resort`](resort) object. The following table lists the properties that are required when you create a user.

| Property name         | Type     | Description                                            |
|-----------------------|----------|--------------------------------------------------------|
| user_id               | Integer  | The ID of the user to which this resort is assigned.   |
| resort_name           | String   | The name of the resort.                                |
| location              | String   | The location of the resort.                            |
| fresh_powder_inches   | Integer  | The current amount of fresh powder in inches at the resort. |
| traffic_conditions    | String   | A brief description of the current traffic conditions at the resort (e.g., "Light", "Medium", "Heavy"). |

## Sample request

The POST request should look something like this. Replace {server_url} with the actual server URL and include the request body with the details of the new resort.

```js
{
      "user_id": 1,
      "resort_name": "Vail",
      "location": "Eagle",
      "fresh_powder_inches": 10,
      "traffic_conditions": "Heavy"
    }'
```

## Response Body

The following example shows the response. Note that the names should be the same as you used in your **Request Body** and the response should include the new resort's ID. The resort's ID is automatically generated when the resort is created.

```js
{
    "user_id": 1,
    "resort_name": "Vail",
    "location": "Eagle",
    "fresh_powder_inches": 10,
    "traffic_conditions": "Heavy",
    "id": 1234
}

```

## Return Status

| Status value    | Return status         | Description                                    |
|-----------------|-----------------------|------------------------------------------------|
| 201             | Created               | Resort was successfully added.                 |
| 400             | Bad Request           | The request was invalid or missing parameters. |
| 500             | Internal Server Error | An error occurred on the server.               |
| ECONNREFUSED    | N/A                   | Service is offline. Start the service and try again. |
