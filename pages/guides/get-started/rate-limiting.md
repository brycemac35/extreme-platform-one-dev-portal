---
source: https://developer.extremeplatformone.com/content/guides/get-started/rate-limiting.md
---

---
title: "Rate Limiting"
---

Extreme Platform ONE enforces API rate limiting to ensure fair usage and system stability. This guide explains the rate limit headers based on the [IETF RateLimit Headers Standard](https://datatracker.ietf.org/doc/draft-ietf-httpapi-ratelimit-headers/).

## Overview

Rate limiting protects the platform by controlling how many API requests a client can make within a given time period. When you exceed your rate limit, the API returns an HTTP 429 (Too Many Requests) response.

## Rate Limit Policies

Rate limit policies are configured when generating an API key. You can use tenant-level defaults or override them at the API key level.

### Available Policies

| Policy Name | Scope | Required | Description |
|-------------|-------|----------|-------------|
| `tenant-hour` | Tenant | Yes | Hourly quota shared across all API keys for the tenant (default: 7,500 requests/hour) |
| `tenant-second` | Tenant | No | Per-second quota shared across all API keys for the tenant |
| `token-hour` | API Key | No | Hourly quota for the specific API key |
| `token-second` | API Key | No | Per-second quota for the specific API key |

### Policy Scopes

- **Tenant-level policies** (`tenant-hour`, `tenant-second`): Quota is shared across all API keys belonging to the same tenant
- **Token-level policies** (`token-hour`, `token-second`): Quota applies only to the specific API key

## Rate Limit Headers

Every API response may include rate limit headers following the [IETF RateLimit Headers](https://datatracker.ietf.org/doc/draft-ietf-httpapi-ratelimit-headers/) standard using the [Structured Fields](https://www.rfc-editor.org/rfc/rfc9651) format.

### Header Format

Both headers use the Structured Fields format with a policy name followed by parameters:

```
Header-Name: "policy-name";param1=value1;param2=value2
```

### RateLimit

Conveys the current rate limit status. This header is **always returned** in API responses.

```http
RateLimit: "tenant-hour";r=7499
```

#### Parameters

| Parameter | Required | Description |
|-----------|----------|-------------|
| `r` | Yes | **Remaining** - Number of requests remaining in the current window |
| `t` | Conditional | **Reset** - Seconds until the quota resets. Only included when `r=0` (quota exhausted) |

#### Behavior

- **When quota is available** (`r > 0`): The `t` parameter is omitted
  ```http
  RateLimit: "tenant-hour";r=7499
  ```

- **When quota is exhausted** (`r = 0`): The `t` parameter indicates seconds until reset
  ```http
  RateLimit: "tenant-hour";r=0;t=60
  ```

When multiple policies are configured, the `RateLimit` header shows the status of the policy with the lowest remaining quota.

### RateLimit-Policy

Defines the server's quota policies. This header is **only returned when quota is exhausted** (`r=0`) and lists **all configured policies** for the current API key.

```http
RateLimit-Policy: "tenant-hour";q=7500;w=3600
```

With multiple policies configured:

```http
RateLimit-Policy: "tenant-hour";q=7500;w=3600, "token-second";q=10;w=1
```

#### Parameters

| Parameter | Required | Description |
|-----------|----------|-------------|
| `q` | Yes | **Quota** - Total number of requests allocated in the time window |
| `w` | Yes | **Window** - Time window duration in seconds |

## Token Bucket Algorithm

Extreme Platform ONE uses the **token bucket algorithm** for rate limiting. This algorithm provides smooth rate limiting while allowing short bursts of traffic.

### How It Works

1. **Bucket initialization**: Each policy has a bucket that holds tokens. The bucket starts full with the quota (`q`) amount of tokens.

2. **Token consumption**: Each API request consumes one token from the bucket. If tokens are available, the request proceeds immediately.

3. **Token replenishment**: Tokens are added to the bucket at a constant rate. The rate is calculated as quota divided by window (`q` ÷ `w`).

4. **Bucket capacity**: The bucket cannot hold more than the quota amount. Tokens added when the bucket is full are discarded.

5. **Request rejection**: When the bucket is empty (no tokens available), requests are rejected with HTTP 429 until tokens are replenished.

### Example

For a `tenant-hour` policy with 7,500 requests per hour (`q=7500;w=3600`):

| Metric | Value |
|--------|-------|
| Bucket capacity | 7,500 tokens |
| Replenishment rate | ~2.08 tokens/second (7,500 ÷ 3,600) |
| Burst capability | Up to 7,500 requests instantly (if bucket is full) |
| Sustained rate | ~2.08 requests/second |

### Benefits

- **Burst tolerance**: Allows short bursts of traffic without immediate rejection
- **Smooth limiting**: Provides consistent rate limiting over the time window
- **Fair distribution**: Ensures equitable resource allocation across all clients

## Example Responses

**Normal response with remaining quota:**

```http
HTTP/1.1 200 OK
Content-Type: application/json
RateLimit: "tenant-hour";r=7499
```

**Response when quota is nearly exhausted:**

```http
HTTP/1.1 200 OK
Content-Type: application/json
RateLimit: "tenant-hour";r=10
```

**Response when quota is exhausted (429 error):**

```http
HTTP/1.1 429 Too Many Requests
Content-Type: application/json
Retry-After: 60
RateLimit-Policy: "tenant-hour";q=7500;w=3600
RateLimit: "tenant-hour";r=0;t=60
```

**Response with multiple policies (429 error):**

```http
HTTP/1.1 429 Too Many Requests
Content-Type: application/json
Retry-After: 1
RateLimit-Policy: "tenant-hour";q=7500;w=3600, "token-second";q=10;w=1
RateLimit: "token-second";r=0;t=1
```

## Handle 429 Rate Limit Errors

When you exceed the rate limit, the API returns an HTTP 429 response. Both `RateLimit-Policy` and `RateLimit` headers are included, along with a `Retry-After` header.

### Error Response Format

```http
HTTP/1.1 429 Too Many Requests
Content-Type: application/problem+json
Retry-After: 60
RateLimit-Policy: "tenant-hour";q=7500;w=3600
RateLimit: "tenant-hour";r=0;t=60

{
  "type": "https://ietf-wg-httpapi.github.io/ratelimit-headers/draft-ietf-httpapi-ratelimit-headers.html#quota-exceeded",
  "title": "Rate limit exceeded",
  "detail": "Request quota exceeded for policy 'tenant-hour'",
  "violated-policies": ["tenant-hour"]
}
```

### Problem Types

The API uses standardized problem types for rate limit errors:

| Problem Type | HTTP Status | Description |
|--------------|-------------|-------------|
| `quota-exceeded` | 429 | Request quota has been exceeded |
| `temporary-reduced-capacity` | 503 | Server capacity temporarily reduced |
| `abnormal-usage-detected` | 429 | Unusual request patterns detected |

### Monitoring Rate Limits

To proactively avoid hitting rate limits, your client should monitor the `RateLimit` header in every API response.

#### Parsing the RateLimit Header

The `RateLimit` header follows the Structured Fields format:

```
RateLimit: "policy-name";r=<remaining>[;t=<reset>]
```

Extract the following values:

| Value | How to Extract | Description |
|-------|----------------|-------------|
| Policy name | Text between quotes (`"..."`) | Identifies which policy is reported |
| Remaining (`r`) | Number after `r=` | Requests remaining in current window |
| Reset (`t`) | Number after `t=` (if present) | Seconds until quota resets (only when `r=0`) |

#### Recommended Monitoring Actions

| Condition | Recommended Action |
|-----------|-------------------|
| `r` is high | Continue normal operations |
| `r` is low (e.g., < 100) | Reduce request frequency or alert operations team |
| `r = 0` | Stop requests and wait for reset time (`t` seconds) |

### Implementing Retry Logic

When your client receives an HTTP 429 response, implement retry logic to recover gracefully.

#### Determining Wait Time

Use the following priority order to determine how long to wait before retrying:

1. **`Retry-After` header** (highest priority): If present, use this value in seconds
2. **`t` parameter in `RateLimit` header**: Extract the reset time from the `RateLimit` header
3. **Default fallback**: Use a reasonable default (e.g., 60 seconds)

#### Retry Strategy Recommendations

| Strategy | Description |
|----------|-------------|
| **Respect headers** | Always honor `Retry-After` and `t` values; do not retry sooner |
| **Maximum retries** | Limit retry attempts (e.g., 3 attempts) to avoid infinite loops |
| **Exponential backoff** | If no reset time is provided, increase wait time between retries |
| **Jitter** | Add random delay to prevent thundering herd when multiple clients retry simultaneously |

#### Important Considerations

- **Do not retry immediately**: Retrying without waiting will result in continued 429 responses
- **Log rate limit events**: Track when rate limits are hit for capacity planning
- **Differentiate policies**: The `RateLimit` header indicates which policy was exhausted; different policies may have different reset times

## Best Practices

- Monitor rate limit headers in every response
- Implement client-side request throttling
- Handle 429 errors with exponential backoff
- Respect the `Retry-After` header (takes precedence over `RateLimit`)
- Do not treat remaining quota (`r`) as a service guarantee
- Use caching to reduce API calls
- Batch requests when possible
- Set up alerts for high rate limit usage

## Next Steps

- [Error Handling](/guides/error-handling) - Handle rate limit errors gracefully
- [Security](/guides/security) - Best practices for secure API usage
