---
layout: page
---

# Tutorial: Create a User

In this tutorial, you will learn how to create a new user in the Powder Alert service database, allowing users to receive real-time alerts about fresh snow at their favorite mountain resorts.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you have completed the setup steps outlined in the [Get Started](../doc/get-started.md) section of the documentation. Ensure you have Postman installed on your system or have access to a similar API testing tool.

## Create a User

Creating a user in the Powder Alert service involves sending a POST request to the appropriate endpoint with the necessary user information.

To create a user:

1. Ensure your local service is running. If not, start it by navigating to the API directory and running the server.

    ```shell
    cd <your-github-workspace>/ski-powder-alert-service/api
    json-server -w to-do-db-source.json
    ```

2. Open the Postman app on your desktop.

3. Create a new request with the following values:
    - **Method**: POST
    - **URL**: `{server_url}/users`
    - **Headers**: `Content-Type: application/json`
    - **Body**: Select `raw` and choose `JSON` format

4. In the request body, include the user details in JSON format. For example:

    ```json
    {
      "last_name": "Johnson",
      "first_name": "Larry",
      "email": "l.johnson@example.com",
      "powder_threshold_inches": 6
    }
    ```

5. Click **Send** to make the request.

6. Review the response body. It should contain the newly created user object, including a unique user ID assigned by the service.

### Sample Response

```json
{
  "user_id": "123456",
  "last_name": "Johnson",
  "first_name": "Larry",
  "email": "l.johnson@example.com",
  "powder_threshold_inches": 6,
  "created_at": "2024-06-01T12:34:56Z"
}
```

### Next steps

After completing this tutorial in Postman, you may want to replicate it in your preferred programming language. Adapt the values from this tutorial to the properties and arguments used in making HTTP requests in your chosen language.
