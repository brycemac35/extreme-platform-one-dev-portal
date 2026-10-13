---
source: https://developer.extremeplatformone.com/content/guides/overview/introduction.md
---

---
title: "Extreme Platform ONE APIs"
---

Welcome to the Extreme Platform ONE developer platform! This guide will help you get started with our comprehensive suite of Extreme Platform ONE APIs.

## What is Extreme Platform ONE?

Extreme Platform ONE is the first all-in-one networking platform powered by conversational, multimodal, and agentic AI.

## Getting Started

To start using Extreme Platform ONE APIs, follow these steps:

1. **Create an Account**: Sign up for an Extreme Platform ONE account
2. **Generate API Keys**: Create API keys for authentication
3. **Make Your First API Call**: Test the APIs with a simple request
4. **Explore API Reference**: Browse our comprehensive API reference

## API Catalog

Our platform provides comprehensive APIs for identity management, device lifecycle, monitoring, and more. See the [API Reference](/api-reference) for the complete list of available services and applications.

## Authentication

All API requests require authentication using an **API key** - a long-lived credential for headless clients, such as scripts, backend tasks, or other tools without GUI. Pass it in the `Authorization` header:

```http request
Authorization: Bearer YOUR_API_KEY
```

Learn more in the [Authentication](/guides/authentication) guide.

## API Versioning

All our APIs are versioned to ensure stability and backward compatibility:

- Current version: **v1**
- API path format: `/{service}/{version}/{endpoint}`

## Rate Limiting

To ensure fair usage and system stability, our APIs implement rate limiting:

- **Per-hour limit**: 7500 requests/hour

Rate limit headers are included in all responses. See [Rate Limiting](/guides/rate-limiting) for details.

## Support & Resources

- **[API Reference](/api-reference)**: Comprehensive documentation for all endpoints
- **[SDKs & Tools](/sdks)**: Official client libraries and development tools
- **Support**: Contact our support team for assistance

## Next Steps

Ready to start building? Here are some recommended next steps:

1. [Quick Start Guide](/guides/quickstart) - Get up and running in 5 minutes
2. [Authentication](/guides/authentication) - Learn how to authenticate
3. [Best Practices](/guides/security) - Learn best practices and patterns
