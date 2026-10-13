---
source: https://developer.extremeplatformone.com/content/guides/best-practices/error-handling.md
---

---
title: "Error Handling"
---

Building robust applications requires comprehensive error handling. This guide covers strategies for handling errors, implementing retry logic, and debugging API issues.

## Always Handle Errors

Never assume API calls will succeed. Implement comprehensive error handling:

```javascript
try {
  const data = await apiClient.get('https://${API_DOMAIN}/iam/v1/myaccount');
  // Process data
} catch (error) {
  if (error.response) {
    // Server responded with error
    console.error('API Error:', error.response.status, error.response.data);
  } else if (error.request) {
    // No response received
    console.error('Network Error:', error.message);
  } else {
    // Request setup error
    console.error('Request Error:', error.message);
  }
}
```

## Implement Retry Logic

Use exponential backoff for transient failures (HTTP 5xx) or implement a more sophisticated retry strategy with jitter.

## Handle 429 Rate Limit Errors

Respect retry-after headers when rate limited.

Learn more about API rate limits in the [Rate Limiting](/guides/rate-limiting) guide.

## Log Trace IDs

Always log Trace IDs for debugging and support. Every API response includes a unique Trace ID in the `X-Trace-ID` header:

```javascript
try {
  const response = await apiClient.get('https://${API_DOMAIN}/iam/v1/myaccount');
  const traceId = response.headers['X-Trace-ID'];
  console.log(`Request ${traceId}:`, response.data);
} catch (error) {
  const traceId = error.response?.headers['X-Trace-ID'];
  console.error(`Request ${traceId} failed:`, error.response?.data);
}
```

Learn more about Trace IDs in the [Trace ID for Troubleshooting](/guides/trace-id) guide.

## Next Steps

- [Rate Limiting](/guides/rate-limiting) - Learn about API rate limits
- [Security](/guides/security) - Best practices for secure API usage
- [HTTP Status Codes](/guides/status-code) - Understand API response codes
- [Trace ID](/guides/trace-id) - Use Trace ID for troubleshooting
