---
source: https://developer.extremeplatformone.com/content/guides/get-started/quickstart.md
---

---
title: "Quick Start Guide"
---

Get started with Extreme Platform ONE APIs in just a few minutes! This guide will walk you through the essential steps to make your first API call.

## Overview

This quick start guide covers:

- Creating your account
- Generating API keys
- Making your first API call
- Understanding the response

## Prerequisites

Before you begin, make sure you have:

- An active Extreme Platform ONE account
- Basic understanding of RESTful APIs
- Familiarity with JSON data format
- An HTTP client (cURL, Postman, or programming language HTTP library)

## Step 1: Create an Account

If you don't already have an account:

1. Visit [Extreme Platform ONE](${EP1_URL})
2. Click **Register to Get Started** to create a new account
3. Verify your email address
4. Complete your account setup and link **CUID**.

## Step 2: Generate an API Key

API keys are required for authenticating your requests:

1. Log in to your Extreme Platform ONE account
2. Navigate to **Administration & Settings** > **Integrations**
3. Click **Create New API Key**
4. Set `Name`, `Decription` and `Expiration Date`, then click **Generate Key**
5. Click **Copy API Key** and securely store your API key

> **Important**: API keys are shown only once. Store them securely!

## Step 3: Make Your First API Call

Let's test the API with a simple request to get your account information:

### Using cURL

```bash
curl -X GET \
  https://${API_DOMAIN}/iam/v1/myaccount \
  -H 'Authorization: Bearer YOUR_API_KEY'
```

### Using JavaScript

```javascript
const response = await fetch('https://${API_DOMAIN}/iam/v1/myaccount', {
  method: 'GET',
  headers: {
    'Authorization': 'Bearer YOUR_API_KEY',
    'Content-Type': 'application/json'
  }
});

const data = await response.json();
console.log(data);
```

### Using Python

```python
import requests

url = "https://${API_DOMAIN}/iam/v1/myaccount"
headers = {
    "Authorization": "Bearer YOUR_API_KEY",
    "Content-Type": "application/json"
}

response = requests.get(url, headers=headers)
print(response.json())
```

## Step 4: Understanding the Response

A successful response will look like this:

```json
{
  "email": "yourname@yourcompany.com",
  "first_name": "Your first name",
  "last_name": "Your last name",
  "job_title": "Your title",
  "locale": "en",
  ...
}
```

## Next Steps

Congratulations! You've made your first API call. Here's what to explore next:

1. [Authentication](/guides/authentication) - Learn more about authentication methods
2. [API Reference](/api-reference) - Explore all available endpoints
3. [Best Practices](/guides/security) - Learn recommended patterns

## Need Help?

- Check our [API Reference](/api-reference) for detailed endpoint documentation
- Contact [Support](mailto:${SUPPORT_EMAIL}) for assistance
