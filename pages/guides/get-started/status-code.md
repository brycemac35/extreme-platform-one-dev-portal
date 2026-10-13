---
source: https://developer.extremeplatformone.com/content/guides/get-started/status-code.md
---

---
title: "HTTP Status Codes"
---

Understanding HTTP status codes is essential for working with Extreme Platform ONE APIs. This guide explains the status codes you'll encounter and how to handle them.

## Success Codes (2xx)

### 200 OK
The request was successful and the server returned the requested data.

### 201 Created
A new resource was successfully created. The response typically includes the newly created resource.

### 204 No Content
The request was successful but there's no content to return (common for DELETE operations).

## Client Error Codes (4xx)

### 400 Bad Request
The request is malformed or contains invalid parameters.

**Common causes:**
- Invalid JSON syntax
- Missing required fields
- Invalid field values

**How to fix:**
- Validate your request body against the API schema
- Check that all required parameters are included
- Ensure data types match the API specification

### 401 Unauthorized
Authentication failed or wasn't provided.

**Common causes:**
- Missing API key or access token
- Expired access token
- Invalid credentials

**How to fix:**
- Verify your API key is correct
- Check if your access token has expired
- Ensure the `Authorization` header is properly formatted

### 403 Forbidden
You're authenticated but don't have permission to access the resource.

**Common causes:**
- Insufficient permissions for the requested operation
- API key doesn't have required scopes
- Trying to access another organization's resources
- Trying to access the APIs requires specific license

**How to fix:**
- Check your licenses
- Verify you're accessing resources within your organization
- Contact support if you need additional permissions

### 404 Not Found
The requested resource doesn't exist.

**Common causes:**
- Incorrect endpoint URL
- Resource has been deleted
- Invalid resource ID

**How to fix:**
- Verify the endpoint URL is correct
- Check that the resource ID exists
- Ensure you're using the correct API version

### 429 Too Many Requests
You've exceeded the rate limit.

**Common causes:**
- Sending too many requests in a short time
- Not implementing exponential backoff for retries

**How to fix:**
- Implement rate limiting in your application
- Use exponential backoff for retries
- Cache responses when possible
- See the [Rate Limiting](/guides/rate-limiting) guide for best practices

**Response headers:**
```http request
X-RateLimit-Limit: 7500
X-RateLimit-Remaining: 0
X-RateLimit-Reset: 600
```

## Server Error Codes (5xx)

### 500 Internal Server Error
Something went wrong on the server side.

**How to handle:**
- Retry the request after a short delay
- If the error persists, contact support

### 502 Bad Gateway
The server received an invalid response from an upstream server.

**How to handle:**
- Retry the request
- These are typically temporary issues

### 503 Service Unavailable
The service is temporarily unavailable, usually due to maintenance.

**How to handle:**
- Check the `Retry-After` header for when to retry
- Implement exponential backoff

## Best Practices

### Handle Status Codes Properly

Always check the HTTP status code before processing the response.

### Implement Retry Logic

For 5xx errors and 429 rate limits, implement exponential backoff.

## Quick Reference

| Status Code | Meaning | Action |
|-------------|---------|--------|
| 200 | Success | Process response data |
| 201 | Created | Resource created successfully |
| 204 | No Content | Operation completed, no data returned |
| 400 | Bad Request | Fix request parameters |
| 401 | Unauthorized | Check authentication |
| 403 | Forbidden | Verify permissions |
| 404 | Not Found | Check resource ID/URL |
| 429 | Rate Limited | Implement backoff, reduce request rate |
| 500 | Server Error | Retry with exponential backoff |
| 502 | Bad Gateway | Retry after delay |
| 503 | Service Unavailable | Check Retry-After header, wait and retry |

## Next Steps

- [Authentication](/guides/authentication) - Learn about authentication methods
- [Rate Limiting](/guides/rate-limiting) - Understand rate limits and how to work within them
- [Error Handling](/guides/error-handling) - Learn comprehensive error handling strategies
