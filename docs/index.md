---
layout: page
---

# Powder Alert Service API

Explore the comprehensive documentation for the Powder Alert service, your go-to solution for real-time updates on snowfall levels at various mountain resorts.
The Powder Alert service is a simple cloud-based API. With its two main resources, **users** and **resorts**, the API allows you to:

* **Get Resorts by Powder Threshold Value**: Learn how to query resorts based on specific snowfall thresholds, enabling you to provide users with real-time updates on the best powder conditions.
* **Create and Manage User Profiles**: Understand how to create user accounts, update user information, and manage user preferences.
* **Retrieve Resort Information**: Discover how to access detailed information about various mountain resorts.
* **Set Up Powder Alerts**: Configure and customize alerts to notify users when their specified snowfall conditions are met, ensuring they never miss out on fresh powder.

## Authentication

For v1 of the Powder Alert service, requests do not use any authorization. All endpoints are available to all users and applications.

## Base URL

All requests to the Powder Alert API should be directed to the base URL: <https://api.powderalert.com>

This base URL is the root endpoint for all API interactions, with specific resource paths appended to it.

## Get Started

Ready to dive in? Start with our [Quick Start Guide](quick-start) for a seamless setup experience and your first API call.

## API Reference

Explore the Powder Alert service's two main endpoints - **users** and **resorts** and the supported HTTP operations. The API reference documentation consists of information about the supported endpoints and their parameters.

The following API refernece endpoints are available:

* [Users Resource](api/user-pa)
* [Resorts Resource](/api/resort-pa)
* [Create a user](api/users-create-user)
* [Get user details for all users](api/users-get-all-users)
* [Get user details by user ID](api/users-get-user-by-id)
* [Create a resort](api/resorts-create-resort)
* [Get resort details by resort ID](api/resorts-get-resort-by-id)
* [Get resort preferences for a user](api/resorts-get-resort-by-user-id)

**Note**: In the documentation, the `{server_url}`refers to the URL of a resource. The `{server_url}` value depends on the installation of the service. When running a local test, the `{server_url}` is generally `http://localhost:3000`.

## Tutorials

This series of tutorials will guide you through the process of utilizing the Powder Alert service to its fullest potential. Whether you are a beginner or an experienced developer, these step-by-step guides are designed to help you understand and implement key features of the Powder Alert API effectively.

* [Get Resorts by Powder Threshold Value](tutorials/get-resorts-by-threshold): Query resorts based on specific snowfall thresholds.

* [Manage Alerts](tutorials/manage-alerts)/: Understand how to create and manage user accounts and preferences.

* [Set Up Powder Alerts](tutorials/set-up-powder-alerts): Configure and customize alerts to notify users about specified snowfall conditions.

## Error Handling

The Powder Alert service follows standard HTTP status codes to indicate the success or failure of an API call. For more information about how errors are handled by the API service, refer to the [Error Handling](error-handling) documentation.
