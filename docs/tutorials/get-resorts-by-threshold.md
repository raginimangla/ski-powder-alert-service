---
layout: page
---

# Tutorial: Get Resorts by Powder Threshold Value

In this tutorial, you will learn how to retrieve resorts based on specific snowfall thresholds, enabling you to provide real-time updates to users on the best powder conditions.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you have completed the setup steps outlined in the [Get Started](../doc/get-started.md) section of the documentation. Ensure you have Postman installed on your system or have access to a similar API testing tool.

## Retrieve resorts by powder threshold value

Retrieving resorts based on a specific powder threshold value from the Powder Alert service requires sending a GET request to the appropriate endpoint with the desired threshold value.

To retrieve resorts by powder threshold value:

1. Ensure your local service is running. If not, start it by navigating to the API directory and running the server.

    ```shell
    cd <your-github-workspace>/ski-powder-alert-service/api
    json-server -w to-do-db-source.json
    ```

2. Open the Postman app on your desktop.

3. Create a new request with the following values:
    - **Method**: GET
    - **URL**: `{server_url}/resorts?powder_threshold=<threshold_value>`
        - **Note**: Replace `<threshold_value>` with the desired snowfall threshold value (e.g., 12 for 12 inches of snow)
    - **Headers**: `Content-Type: application/json`

4. Click **Send** to make the request.

5. Review the response body, which should contain an array of resorts that meet the specified powder threshold criteria. Each resort object should include details such as name, location, current snowfall, and other relevant information.

### Sample Response

```json
[
    {
        "resort_name": "Vail",
        "county": "Eagle",
        "fresh_powder_inches": 12,
        "traffic_conditions": "heavy",
        "id": 1
    },
    {
        "resort_name": "Breckenridge",
        "county": "Summit",
        "fresh_powder_inches": 12,
        "traffic_conditions": "moderate",
        "id" : 4
    }
]