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
All requests to the Powder Alert API should be directed to the base URL: https://api.powderalert.com

This base URL is the root endpoint for all API interactions, with specific resource paths appended to it.

## Get Started




## API Reference
The API reference docs refer to a `{base_url}` when they refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When running a local test, the `{base_url}` is generally `http://localhost:3000`.

* [users resource](api/user)
* [resorts resource](api/resorts)
