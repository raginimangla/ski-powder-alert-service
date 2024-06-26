---
layout: page
---
# `resort` resource

Base endpoint

```shell
{server_url}/resorts
```

Contains resort information.

## Resource properties

Sample `resort` resource

```js

{
      "user_id": 1,
      "resort_name": "Vail",
      "county": "Eagle",
      "fresh_powder_inches": "10",
      "traffic_conditions": "heavy",
      "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | Integer | The ID of the user resources to which this resort is assigned. |
| `resort_name` | String | The name of the resort. |
| `location` | String | The location of the resort. |
| `fresh_powder_inches` | Integer | The current amount of fresh powder in inches at a resort. When this value exceeds a user's `powder_threshold_inches` value, the user receives an alert. |
| `traffic_conditions` | String | A brief description of the current traffic conditions at a resort (e.g. "Light", "Medium", "Heavy"). |
| `id` | Integer | The resort's unique record ID. |

## Operations

The `resort` resource supports these operations.

### READ (GET)

* [Get all Resorts](/ski-powder-alert-service/api/resorts-get-resort-by-user-id)
* [Get Resort by ID](/ski-powder-alert-service/api/resorts-get-resort-by-id)
* [Get Resorts by User ID](/ski-powder-alert-service/api/resorts-get-resort-by-user-id)

### CREATE (POST)

* [Create a Resort](/ski-powder-alert-service/api/resorts-create-resort)

### UPDATE (PUT/PATCH)

* [Update a Resort](/ski-powder-alert-service/api/update-resort-by-id)
