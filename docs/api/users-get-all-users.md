---
layout: page
---

# Get All Users

Retrieve a list of all registered users. This endpoint allows you to fetch information about all users within the system.

## URL

```shell

{GET}{server_url}/users/
```

## Request headers

None

## Request Body

None

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
      "last_name": "Meyer",
      "first_name": "Cornelius",
      "email": "c.meyer@example.com",
      "powder_threshold_inches": 8,
      "id": 2
    }
        {
      "last_name": "Patel",
      "first_name": "Anita",
      "email": "a.patel@example.com",
      "powder_threshold_inches": 6,
      "id": 3
    },
    {
      "last_name": "Garcia",
      "first_name": "Jorge",
      "email": "j.garcia@example.com",
      "powder_threshold_inches": 12,
      "id": 4
    },
    {
      "last_name": "Lombardo",
      "first_name": "Hector",
      "email": "h.lombardo@example.com",
      "powder_threshold_inches": 10,
      "id": 4
    }
]
```

## Return Status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 201 | Created | User data created successfully. |
| 500 | Internal server Error | Invalid JSON. |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
