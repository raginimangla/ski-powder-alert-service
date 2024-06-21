---
layout: page
---

# Get User Details by User ID

Retrieve detailed information about a specific user by their user ID. This endpoint allows you to fetch the profile details of a particular user.

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

No request body is needed for this GET request. The user ID should be specified in the URL path.

## Sample request

The GET body should look something like this. Replace {user_id} with the actual user ID. Note that the headers are optional and can be included as needed.

```shell
curl -X GET https://api.powderalert.com/v1/users/{user_id}
```

or, if using headers:

```shell

curl -X GET https://api.powderalert.com/v1/users/{user_id} \
-H "Content-Type: application/json" \
-H "Accept: application/json"
```

## Response Body

The following example shows the response.

```js
{
  "user_id": "123456",
  "last_name": "Patel",
  "first_name": "Anita",
  "email": "a.patel@example.com",
  "powder_threshold_inches": 6,
  "created_at": "2024-06-01T12:34:56Z"
}

```

## Return Status

| Status value    | Return status         | Description                                    |
|-----------------|-----------------------|------------------------------------------------|
| 200             | OK                    | Request was successful and users were returned.|
| 400             | Bad Request           | The request was invalid or missing parameters. |
| 500             | Internal Server Error | An error occurred on the server.               |
| ECONNREFUSED    | N/A                   | Service is offline. Start the service and try again. |
