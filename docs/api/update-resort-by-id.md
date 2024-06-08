---
layout: page
---

# Update a Resort By ID

Update an existing resort in the system by using the resort ID. This endpoint allows you to modify details such as the resort name, location, current fresh powder inches, and traffic conditions.

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

The PATCH request should look something like this. Replace `{server_url}` and `{resort_id}`with the actual server URL and the resort ID, and include the request body with the details of the resort to be updated.

```js
{
      "user_id": 1,
      "resort_name": "Hill Country",
      "location": "Texas",
      "fresh_powder_inches": 12,
      "traffic_conditions": "Medium"
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
