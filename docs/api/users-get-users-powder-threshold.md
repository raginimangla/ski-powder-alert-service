---
layout: page
---

# Get Users by Powder Threshold

Retrieve a list of users who have set a powder threshold limit. This endpoint allows you to query users based on their specified snowfall threshold, enabling you to see which users will receive alerts when the threshold is met.

## URL

```shell

{GET}{server_url}/users/{user_id}
```

## Request headers

This request does not use any authorization. The endpoint is available to all users and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data to be posted. | Optional | application/json. Default value.  |
| Accept | The format of the data to be returned. | Optional | application/json. Default value. |

## Request Body

No request body is needed for this GET request. The threshold is specified as a query parameter in the URL.

## Sample request

The GET request should look something like this. Replace {server_url} with the actual server URL.

```bash

curl -X GET "{server_url}/v1/users?threshold=6" \
-H "Content-Type: application/json" \
-H "Accept: application/json"
```

## Response Body

The following example shows the response.

```js
[
    {
        "last_name": "Johnson",
        "first_name": "Larry",
        "email": "l.johnson@example.com",
        "powder_threshold_inches": 6,
        "id": 1

    }
    {
        "last_name": "Patel",
        "first_name": "Anita",
        "email": "a.patel@example.com",
        "powder_threshold_inches": 6,
        "id": 3
    }
]
```

## Return Status

| Status value    | Return status         | Description                                    |
|-----------------|-----------------------|------------------------------------------------|
| 200             | OK                    | Request was successful and users were returned.|
| 400             | Bad Request           | The request was invalid or missing parameters. |
| 500             | Internal Server Error | An error occurred on the server.               |
| ECONNREFUSED    | N/A                   | Service is offline. Start the service and try again. |

## Related information

* [Handling errors](handling-errors.md)
