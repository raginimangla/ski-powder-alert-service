---
layout: page
---
# Get all Resorts

Retrieve detailed information about all resorts. This endpoint allows you to query and get information such as resort names, locations, current powder inches, and traffic conditions for all resorts.

## URL

```shell
{GET} {server_url}/resorts
```

## Request Headers

This request does not use any authorization. The endpoint is available to all users and applications.

|Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data to be posted. | Optional | application/json. Default value.  |
| Accept | The format of the data to be returned. | Optional | application/json. Default value. |

## Request Body

No request body is needed for this GET request.

## Sample Request

The GET request should look something like this. Replace {server_url} with the actual server URL. Note that the headers are optional and can be included as needed.

```shell
curl -X GET "{server_url}/resorts"
```

or, if using headers:

```shell
curl -X GET "{server_url}/resorts" \
-H "Content-Type: application/json" \
-H "Accept: application/json"
```

## Response Body

The following example shows the response:

```json
[
    {
        "user_id": 1,
        "resort_name": "Vail",
        "location": "Eagle",
        "fresh_powder_inches": 10,
        "traffic_conditions": "Heavy",
        "id": 1
    },
    {
        "user_id": 2,
        "resort_name": "Aspen",
        "location": "Pitkin",
        "fresh_powder_inches": 4,
        "traffic_conditions": "Medium",
        "id": 2
    }
]
```

## Return Status

| Status value  | Return status         | Description                                        |
|---------------|-----------------------|----------------------------------------------------|
| 200           | OK                    | Request was successful and the resorts were returned. |
| 400           | Bad Request           | The request was invalid or missing parameters.    |
| 404           | Not Found             | No resorts were found.                            |
| 500           | Internal Server Error | An error occurred on the server.                  |
| ECONNREFUSED  | N/A                   | Service is offline. Start the service and try again. |
