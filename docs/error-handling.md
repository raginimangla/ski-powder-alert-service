---
layout: page
---

# Error Handling in Powder Alert Service

The Powder Alert service follows standard HTTP status codes to indicate the success or failure of an API call. This topic will help you understand the different types of errors that may occur and how to handle them effectively.

## HTTP Status Codes

The Powder Alert Service uses standard HTTP status codes to indicate the outcome of an API request. Here are the most common status codes you might encounter:

### Success Codes

| Status Code | Description                                       |
|-------------|---------------------------------------------------|
| 200 OK      | The request was successful, and the server returned the requested data. |
| 201 Created | The request was successful, and a new resource was created. |
| 204 No Content | The request was successful, but there is no content to send in the response. |

### Client Error Codes

| Status Code | Description                                       |
|-------------|---------------------------------------------------|
| 400 Bad Request | The server could not understand the request due to invalid syntax. This often occurs when required parameters are missing or malformed. |
| 401 Unauthorized | The request requires user authentication. Ensure that the request includes the necessary authentication credentials. |
| 403 Forbidden | The server understood the request, but the client does not have permission to access the resource. |
| 404 Not Found | The requested resource could not be found. Verify that the endpoint and parameters are correct. |
| 405 Method Not Allowed | The request method is not supported for the requested resource. |
| 422 Unprocessable Entity | The server understands the content type of the request entity, but it was unable to process the contained instructions. This often indicates a validation error. |

### Server Error Codes

| Status Code | Description                                       |
|-------------|---------------------------------------------------|
| 500 Internal Server Error | The server encountered an unexpected condition that prevented it from fulfilling the request. |
| 502 Bad Gateway | The server received an invalid response from an upstream server. |
| 503 Service Unavailable | The server is currently unavailable (overloaded or down for maintenance). |

## Error Response Format

When an error occurs, the Powder Alert Service returns a JSON response containing details about the error. The response typically includes the following fields:

```json
{
  "status": "error",
  "code": 400,
  "message": "Invalid request parameters",
  "details": {
    "parameter": "powder_threshold",
    "message": "Powder threshold must be a positive integer"
  }
}

### Response Fields

| Field    | Description                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| status   | Indicates the status of the response (e.g., "error").                                         |
| code     | The HTTP status code associated with the error.                                               |
| message  | A brief description of the error.                                                             |
| details  | Additional information about the error, which may include specific parameters or validation messages. |

## Handling Errors in Your Application

To handle errors effectively in your application:

1. **Check the Status Code**: Inspect the HTTP status code of the response to determine if the request was successful or if an error occurred.
2. **Parse the Error Response**: If an error occurred, parse the JSON response to extract details about the error.
3. **Implement Retry Logic**: For transient errors (e.g., 502 or 503), implement retry logic to handle temporary issues.
4. **Log Errors**: Log error details to help with debugging and to monitor the health of your application.
5. **Provide User Feedback**: Inform users about the error and, if possible, provide actionable steps to resolve the issue.
