---

layout: page

---

# Tutorial: Set Up Powder Alerts

In this tutorial, you will learn how to configure and customize alerts to notify users when their specified snowfall conditions are met, ensuring they never miss out on fresh powder.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you have completed the setup steps outlined in the [Get Started](../doc/get-started.md) section of the documentation. Ensure you have Postman installed on your system or have access to a similar API testing tool.

## Set Up Powder Alerts

Setting up powder alerts in the Powder Alert service requires sending a POST request to the appropriate endpoint with the desired alert configuration.

To set up powder alerts:

1. Ensure your local service is running. If not, start it by navigating to the API directory and running the server.

    ```shell
    cd <your-github-workspace>/ski-powder-alert-service/api
    json-server -w to-do-db-source.json
    ```

2. Open the Postman app on your desktop.

3. Create a new request with the following values:

    - **Method**: POST
    - **URL**: `{server_url}/alerts`
    - **Headers**: `Content-Type: application/json`
    - **Body**: JSON (raw)

    ```json
    {
        "user_id": 1,
        "resort_id": 2,
        "powder_threshold": 12,
        "notification_method": "email"
    }
    ```

4. Click **Send** to make the request.

5. Review the response body, which should confirm the creation of the alert with the specified criteria.

### Sample Response

```json
{
    "alert_id": 1,
    "user_id": 1,
    "resort_id": 2,
    "powder_threshold": 12,
    "notification_method": "email"
}
