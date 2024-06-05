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

* [Get all resorts](#resource-properties)
* [Get resort by ID](resorts-get-resort-by-id.md)
* [Get resorts by user ID](resorts-get-resort-by-user-id.md)
* [Get resorts by name](resorts-get-resort-by-name)
* [Get resorts by amount of fresh powder](resorts-get-resorts-by-amount-of-fresh-powder)

### CREATE (POST)

* [Add a resort](resorts-add-resort.md/)

### UPDATE (PUT/PATCH)

* [Update a resort with PATCH](update-resort-with-patch.md)
