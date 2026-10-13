---
source: https://developer.extremeplatformone.com/content/guides/get-started/trace-id.md
---

---
title: "Trace ID for Troubleshooting"
---

Every API request to Extreme Platform ONE includes a unique **Trace ID** that helps you troubleshoot issues, track requests across distributed systems, and get faster support from our team.

## What is a Trace ID?

A Trace ID is a unique 32-character hexadecimal identifier automatically generated for every API request. It follows the OpenTelemetry trace ID format and enables end-to-end request tracing across our distributed system.

**Example**: `4bf92f3577b34da6a3ce929d0e0e4736`

The Trace ID is included in:
- **All HTTP Response Header**: `X-Trace-ID` header
- **Error Response Body**: `trace_id` field

## Why Trace ID Matters

Trace IDs are essential for:

- **Faster Support**: Provide the Trace ID when contacting customer support to help us quickly locate logs and diagnose issues
- **Request Tracking**: Correlate a single request across multiple microservices and log systems
- **Debugging**: Link frontend errors to backend logs for comprehensive troubleshooting
- **Performance Analysis**: Identify slow requests and trace them through the entire system
- **Audit Trail**: Maintain a complete record of API interactions for compliance and security

## How to Find Your Trace ID

### From HTTP Response Headers

The `X-Trace-ID` header is included in every API response header:

```http request
HTTP/2 200
Content-Type: application/json
X-Trace-ID: 4bf92f3577b34da6a3ce929d0e0e4736
Date: Tue, 12 Nov 2024 10:30:00 GMT
```

### From Error Response Body

```json
{
  "error": {
    "code": "UNAUTHORIZED",
    "message": "Invalid access token or API key",
    "trace_id": "4bf92f3577b34da6a3ce929d0e0e4736",
    "timestamp": 1699564800
  }
}
```

## Best Practices

### DO

- ✅ **Log the Trace ID** for every API request in your application logs
- ✅ **Include Trace ID in error messages** to make troubleshooting easier
- ✅ **Provide Trace ID when contacting support** - it helps us locate your request instantly
- ✅ **Store Trace ID with transaction records** for audit trails and compliance
- ✅ **Use Trace ID to correlate errors** between frontend and backend systems

### DON'T

- ❌ **Don't parse or interpret the Trace ID value** - treat it as an opaque identifier
- ❌ **Don't use Trace ID as a security token** - it's not secret and not meant for authentication
- ❌ **Don't use Trace ID for duplicate detection** - use idempotency keys instead (retrying a request generates a new Trace ID)

## FAQ

### Can I use Trace ID to detect duplicate requests?

No. Each API request generates a unique Trace ID, even if you retry the same operation.

For duplicate detection, use:
- **Idempotency keys** in request headers
- **Client-generated unique identifiers** for operations
- **Transaction IDs** managed by your application

The Trace ID is for **troubleshooting and tracing**, not for business logic.

## Contacting Support

When reporting API issues to Extreme Networks support, always includes the Trace ID:

```text
Subject: Extreme Platform ONE API Error - [Trace ID: 4bf92f3577b34da6a3ce929d0e0e4736]

Trace ID: 4bf92f3577b34da6a3ce929d0e0e4736

[Additional details about what you were trying to do]
```

The Trace ID allows our team to:
- Instantly locate your request in our logs
- See the complete request flow across all services
- Identify the exact point of failure
- Provide faster and more accurate assistance

## Related Topics

- [Error Handling](/guides/error-handling) - Learn how to handle API errors gracefully
- [HTTP Status Codes](/guides/status-code) - Understand API response codes
- [Authentication](/guides/authentication) - Troubleshoot authentication issues
- [API Reference](/api-reference) - Explore all available endpoints
