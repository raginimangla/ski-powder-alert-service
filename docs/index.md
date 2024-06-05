---
layout: page
---

# Powder Alert Service API

 Powder Alert API service allows you to access information about snowfall at mountain resorts, helping you chase the freshest powder. Whether you're developing a mobile app, a web service, or integrating into a larger system, the Powder Alert service provides the tools you need to keep your users informed and ready for the slopes.

The Powder Alert service is a simple cloud-based API. With its two main resources, **users** and **resorts**, the API allows you to:

* Create and manage user profiles.
* Retrieve detailed information about specific resorts.
* Set up and customize powder alerts based on snowfall thresholds.
* Receive notifications when your specified conditions are met.

## Authenticate

Users authenticate into the service using their username and password.

## Base URL

All requests to the Powder Alert API should be directed to the base URL: <https://api.powderalert.com>

This base URL is the root endpoint for all API interactions, with specific resource paths appended to it.

## Get Started

Ready to dive into the Powder Alert API? Follow these simple steps to set up your development environment and make your first query to receive the latest powder threshold levels at your favorite resort.

### Step 1: Set up your development environment

1. **Install a Code Editor**: Download and install a code editor, such as Visual Studio Code, if you don’t already have one.

2. **Set Up a Command Line Interface (CLI)Tool**:

* macOS/Linux: Terminal is pre-installed.
* Windows: Command Prompt or PowerShell is pre-installed.

1. **Install cURL**:

* macOS: cURL is pre-installed.
* Linux: Install cURL using your package manager (e.g., sudo apt install curl).
* Windows: Download and install cURL from the official site.

**Note**: Alternatively, you can use Postman for testing API calls with a graphical interface.

### Step 2: Sign up and Authenticate

First, sign up for an account to access the Powder Alert API and then authenticate using your username and password.

### (Optional) Step 3: Explore the Endpoints

The Powder Alert API uses two main endpoints. Refer to the documentation for more details.

* [Users Resource](../api/user-pa.md)
* [Resorts Resource](../api/resort-pa.md)

### Step 4: Set up Your First Powder Alert

* Set up your first powder alert []

## API Reference

The API reference docs refer to a `{base_url}` when they refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When running a local test, the `{base_url}` is generally `http://localhost:3000`.

* [Users Resource](../api/user-pa.md)
* [Resorts Resource](../api/resort-pa.md)
* [Create a user](../api/users-create-user.md)
* [Get user details for all users](../api/users-get-all-users.md)
* [Get user details by user ID](../api/users-get-user-by-id.md)
* [Create a resort](../api/resorts-add-resort.md)
* [Get resort details by resort ID](../api/resorts-get-resort-by-id.md)
* [Get resort preferences for a users](../api/resorts-get-resort-by-user.md)

## Tutorials

text

* [Get resorts by powder threshold value](../tutorials/get-resorts-by-powder-threshold.md)

## Error Handling

The Powder Alert service follows standard HTTP status codes to indicate the success or failure of an API call. Here is an overview of common HTTP status codes and their meanings, along with typical reasons for each code.

Operations that execute successfully will return `2xx` codes. Operations that result in an error due to a problem on the client's side, such as invalid input, will return standard `4xx` codes. Operations that result in an error due to a problem with the server will return `5xx` codes.

### HTTP Status Code Summary

This section summarizes the most frequent HTTP status codes returned by the API and describes their common causes.

| **HTTP Status Code** | Status Text           | Description                                                                                                                                                                 | Common Causes                                                                                                                                             |
| -------------------- | --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **200**              | OK                    | The request succeeded. The exact result depends on the HTTP method used. With `GET`, the requested resource is returned. With `POST`, a new resource is created or updated. | N/A                                                                                                                                                       |
| **400**              | Bad Request           | The request was unacceptable, often due to missing a required parameter or malformed request body.                                                                          | Missing required parameters, malformed JSON, or invalid data formats.                                                                                     |
| **404**              | Not Found             | The requested resource does not exist.                                                                                                                                      | Incorrect endpoint URL, attempting to access non-existent resources, or typo in the request.                                                              |
| **405**              | Method Not Allowed    | The HTTP method used is not supported by the endpoint.                                                                                                                      | Using an inappropriate HTTP method, like sending `GET` instead of `POST`, or trying to delete where only updates are allowed.                             |
| **500**              | Internal Server Error | The server encountered an unexpected condition that prevented it from fulfilling the request.                                                                               | A generic server-side issue, such as a crash, unhandled exceptions, or resource constraints.                                                              |
| **503**              | Service Unavailable   | The server cannot handle the request.                                                                                                            | Server is temporary overloaded or insufficient resources to process the request.                                                                          |
| No Status code       | ECONNREFUSED          | The service refused the connection.                                                                                                                                         | The service is offline, or you're connecting to the wrong port or hostname. Check if the service is running and try again with the correct port/hostname. |
