---
layout: page
---

# Powder Alert Service API

The Powder Alert service is a simple cloud-based API that helps you get real-time updates on snowfall levels at nearby  mountain resorts. This service also enables you to manage user profiles, keep a record of their favorite resorts, and send notifications when a resorts meets a specific threshold level of fresh powder or snow.

The API has two resources, **users** and **resorts**. You can use the Powder Alert service to perform the following key functions:

* **Create and Manage User Profiles**: Create user accounts, update user information, and manage user preferences for fresh powder.
* **Retrieve Resort Information**: Access detailed information about various mountain resorts, including fresh powder (in inches) at each resort .
* **Get Resorts by Powder Threshold Value**: Query resorts based on specific snowfall thresholds.
* **Set Up Powder Alerts**: Configure and customize alerts to notify users when their specified snowfall conditions are met.

## Authentication

The Powder Alert service requests do not use any authorization. All endpoints are available to all users and applications.

## Base URL

All requests to the Powder Alert API should be directed to the base URL: `https://api.powderalert.com`

This base URL is the root endpoint for all API interactions, with specific resource paths appended to it.

## Get Started

Ready to plunge? Use the following [Quick Start Guide](/docs/quick-start.md) to set up your development environment and make your first API call.

## API Reference

Explore the Powder Alert service's two main endpoints - **users** and **resorts** and their supported HTTP operations.

The following API refernece endpoints are available:

* [Users resource](api/user-pa)
* [Resorts resource](/docs/api/resort-pa)
* [Get all users](api/users-get-all-users)
* [Get a user by user ID](api/users-get-user-by-id)
* [Create a resort](api/resorts-create-resort)
* [Get all resorts](api/resorts-get-all-resorts)
* [Get a resort by resort ID](api/resorts-get-resort-by-id)
* [Get a list of resorts assigned to a specific user](api/resorts-get-resort-by-user-id)

**Note**: In this documentation, the `{server_url}`refers to the URL of a resource. The `{server_url}` value depends on the installation of the service. When running a local test, the `{server_url}` is generally `http://localhost:3000`.

## Tutorials

Use these step-by-step tutorials to understand how to implement the key features of the Powder Alert API service effectively.

* [Create a user](tutorials/users-create-user): Create and manage user profiles.
* [Set Up Powder Alerts](tutorials/set-up-powder-alerts): Configure alerts to notify users about their specified snowfall conditions.
* [Manage Alerts](tutorials/manage-alerts): Create and manage user alerts.
* [Get Resorts by Powder Threshold Value](tutorials/get-resorts-by-threshold): Query resorts based on specific snowfall threshold level.

## Error Handling

The Powder Alert service follows standard HTTP status codes to indicate the success or failure of an API call. For more information about how errors are handled by the API service, refer to the [Error Handling](error-handling) documentation.
