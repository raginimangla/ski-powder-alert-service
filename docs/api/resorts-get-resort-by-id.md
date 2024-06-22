---
layout: page
---

# Get a Resort by Resort ID

Retrieve detailed information about a specific resort using its unique ID. This endpoint allows you to query a resort and get information such as resort's name, location, current powder inches, and traffic conditions.

## URL

```shell

{GET}{server_url}/resorts/{resort_id}
```

## Request headers

This request does not use any authorization. The endpoint is available to all users and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data to be posted. | Optional | application/json. Default value.  |
| Accept | The format of the data to be returned. | Optional | application/json. Default value. |

## Request Body

No request body is needed for this GET request. The resort ID is specified as a path parameter in the URL.

## Sample request

The GET request should look something like this. Replace `{server_url}` and `{resort_id}`with the actual server URL and the resort ID. Note that the headers are optional and can be included as needed.

```shell
curl -X GET "{server_url}/resorts/{resort_id}" \
```

or, if using headers:

```shell

curl -X GET "{server_url}/resorts/{resort_id}" \
-H "Content-Type: application/json" \
-H "Accept: application/json"
```

## Response Body

The following example shows the response.

```js
{
    "user_id": 1,
    "resort_name": "Vail",
    "location": "Eagle",
    "fresh_powder_inches": 10,
    "traffic_conditions": "Heavy",
    "id": 1
}


```

## Return Status

| Status value    | Return status         | Description                                    |
|-----------------|-----------------------|------------------------------------------------|
| 200             | OK                    | Request was successful and the resort was returned.|
| 400             | Bad Request           | The request was invalid or missing parameters. |
| 404             | Not Found             | The resort with the specified ID was not found. |
| 500             | Internal Server Error | An error occurred on the server.               |
| ECONNREFUSED    | N/A                   | Service is offline. Start the service and try again. |
