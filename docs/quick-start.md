---
layout: page
---

# Getting Started with Powder Alert Service

Get started with the Powder Alert service to receive real-time updates on snowfall levels at various mountain resorts. This guide will walk you through the setup process, making it easy to start using the service in no time.

## At a Glance

This guide provides all the information you need to begin using the Powder Alert service. You will learn when and how to use the service and get set up to make your first call to the API.

## Setting up the Powder Alert Service

To start receiving alerts about snowfall levels at mountain resorts, follow these steps:

1. **Clone the Repository**: Clone or download the Powder Alert service repository from the provided GitHub link.

2. **Install Dependencies**: Navigate to the API directory and install dependencies:

    ```shell
    cd <path/to/your/repository>/ski-powder-alert-service/api
    npm install
    ```

3. **Start the Server**: Launch the local server by running the following command:

    ```shell
    json-server -w to-do-db-source.json
    ```

4. **Test the Service**: Ensure that the service is running correctly by making a test request to one of the available endpoints using Postman or a similar tool.

## When to Use the Powder Alert Service

The Powder Alert service provides real-time updates on snowfall levels at mountain resorts, making it ideal for various scenarios:

- Ski enthusiasts can stay informed about fresh powder conditions at their favorite resorts.
- Ski resorts can use the service to provide visitors with timely updates on snowfall levels, enhancing their overall experience.

## How to Use the Powder Alert Service

To interact with the Powder Alert service, you will need to:

- **Define a Host**: Set the base URL depending on your installation of the service in your development environment. For example, for v1 of the Powder Alert Service API, the base URL variable is typically set to `http://localhost:3000`.
- **Prepare Authorization**: For v1 of the Powder Alert service, requests do not require any authorization. All endpoints are accessible to all users and applications.
- **Make Requests**: Utilize the Powder Alert service REST API to perform CRUD operations via HTTP requests on database resources. Request and response bodies are encoded as JSON.

### Supported Endpoints

| HTTP Method | Endpoint                                                                                |
|-------------|-----------------------------------------------------------------------------------------|
| GET         | [List all users](/docs/api/users-get-all-users#get-all-users)                                         |
| GET         | [List all resorts](/docs/api/resorts-get-all-resorts)                                                          |
| GET         | [List all users by ID](/docs/api/users-get-user-by-id)                               |
| GET         | [List all users by preferred snow threshold](/docs/api/users-get-users-by-threshold) |
| CREATE      | [Create a user](/docs/api/users-create-user)                                         |
| CREATE      | [Create a resort](/docs/api/resorts-create-resort)                                |
| POST        | [Create an alert](/docs/tutorials/manage-alerts)                        |
| PATCH       | [Update a resort](/docs/api/update-resort-by-id)                     |
| PATCH       | [Update an alert](/docs/tutorials/manage-alerts)                        |

## Next Steps

Now that you've set up the Powder Alert service, you're ready to start receiving real-time updates on snowfall levels at mountain resorts. Experiment with different endpoints and explore how the service can enhance your experience in the snow!

Happy skiing!
