---

layout: page

---

# Tutorial: Manage Alerts

In this tutorial, you will learn how to create, update, and delete alerts for specific resorts in the Powder Alert service. Managing alerts allows users to customize notifications based on their preferred snowfall conditions.

Expect this tutorial to take about 20 minutes to complete.

## Before you start

Make sure you have completed the setup steps outlined in the [Get Started](../doc/get-started.md) section of the documentation. Ensure you have Postman installed on your system or have access to a similar API testing tool.

## Manage Alerts

Managing alerts in the Powder Alert service involves creating, updating, and deleting alerts based on user preferences.

### Create a New Alert

To create a new alert:

1. Open the Postman app on your desktop.

2. Create a new request with the following values:

    - **Method**: POST
    - **URL**: `{server_url}/alerts`
    - **Headers**: `Content-Type: application/json`
    - **Body**: JSON (raw)

    ```json
    {
        "user_id": 1,
        "resort_id": 1,
        "powder_threshold_inches": 6,
        "notification_method": "email",
        "id": 5
    }
    ```

3. Click **Send** to make the request.

4. Review the response body. It should confirm the creation of the alert with the specified criteria.

### Update an Existing Alert

To update an existing alert:

1. Open the Postman app on your desktop.

2. Create a new request with the following values:

    - **Method**: PUT
    - **URL**: `{server_url}/alerts/{alert_id}`
      - **Note**: Replace `{alert_id}` with the ID of the alert you want to update.
    - **Headers**: `Content-Type: application/json`
    - **Body**: JSON (raw)

    ```json
    {
        "user_id": 1,
        "resort_id": 1,
        "powder_threshold_inches": 8,
        "notification_method": "SMS",
         "id": 5
    }
    ```

3. Click **Send** to make the request.

4. Review the response body, which should confirm the update of the alert with the specified changes.

### Delete an Alert

To delete an alert:

1. Open the Postman app on your desktop.

2. Create a new request with the following values:

    - **Method**: DELETE
    - **URL**: `{server_url}/alerts/{alert_id}`
      - (Replace `{alert_id}` with the ID of the alert you want to delete.)

3. Click **Send** to make the request.

4. Review the response body, which should confirm the deletion of the alert.

---

## Next steps

After completing this tutorial in Postman, you may want to replicate it in your preferred programming language. Adapt the values from this tutorial to the properties and arguments used in making HTTP requests in your chosen language.
