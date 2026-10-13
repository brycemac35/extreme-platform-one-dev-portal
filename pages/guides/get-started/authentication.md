---
source: https://developer.extremeplatformone.com/content/guides/get-started/authentication.md
---

---
title: "Authentication"
---

Every Extreme Platform ONE API request must be authenticated with an API key. This guide explains how to create an API key, use it in your requests, and keep it secure.

## How Authentication Works

Extreme Platform ONE authenticates API requests with **API keys** - long-lived credentials ideal for headless clients such as scripts, backend tasks, or other tools without GUI.

Pass your API key in the `Authorization` header using the `Bearer` scheme:

```http request
Authorization: Bearer YOUR_API_KEY
```

Key characteristics:

- The expiration date is set by the user who creates the key.
- A key carries the permissions of the account that created it.
- Requests with a missing, malformed, expired, or revoked key are rejected with `401 Unauthorized`.

## Generating an API Key

To generate an API key:

1. Log in to Extreme Platform ONE
2. Navigate to **Administration & Settings** > **Integrations**
3. Click **Create New API Key** link
4. Provide name, description and expiration date
5. Click **Generate Key** button
6. Copy the generated API key immediately

> **Warning**: API keys are only shown once. Store them securely in a password manager or secrets vault.

## Using Your API Key

The following examples call the `/iam/v1/myaccount` endpoint to retrieve your account information.

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
    'Authorization': `Bearer ${process.env.EXTREME_API_KEY}`,
    'Content-Type': 'application/json'
  }
});

const data = await response.json();
```

### Using Python

```python
import os
import requests

url = "https://${API_DOMAIN}/iam/v1/myaccount"
headers = {
    "Authorization": f"Bearer {os.environ['EXTREME_API_KEY']}",
    "Content-Type": "application/json"
}

response = requests.get(url, headers=headers)
print(response.json())
```

## API Key Lifecycle

| Stage          | What happens                                                                                                              |
|----------------|---------------------------------------------------------------------------------------------------------------------------|
| **Creation**   | You set the name, description, and expiration date. The key value is displayed once.                                        |
| **Active**     | The key authenticates requests until it expires or is revoked.                                                              |
| **Expiration** | After the expiration date, the key stops working and requests return `401 Unauthorized`.                                    |
| **Rotation**   | Generate a new key, deploy it, verify traffic uses it, then revoke the old key.                                             |
| **Revocation** | Revoke a key from **Administration & Settings** > **Integrations**. Revocation takes effect immediately and cannot be undone. |

To avoid downtime, create the replacement key *before* revoking the old one so both are valid during the switch over.

## API Key Best Practices

### DO

- ✅ Store API keys in environment variables or secrets management systems
- ✅ Use different API keys for different applications or environments
- ✅ Rotate API keys regularly (every 90 days recommended)
- ✅ Use the principle of least privilege - grant minimum required permissions
- ✅ Revoke API keys immediately if compromised

### DON'T

- ❌ Hardcode API keys in your source code
- ❌ Commit API keys to version control (Git, SVN, etc.)
- ❌ Share API keys via email or messaging apps
- ❌ Use the same API key across multiple applications
- ❌ Log API keys in application logs

## Storing API Keys Securely

For local development, keep the key in an environment file that is excluded from version control:

```bash
# .env file (never commit this!)
EXTREME_API_KEY=your_api_key_here
EXTREME_API_BASE_URL=https://${API_DOMAIN}
```

```javascript
// Access in your application
const apiKey = process.env.EXTREME_API_KEY;
const baseUrl = process.env.EXTREME_API_BASE_URL;
```

For production applications, use a secrets management service such as AWS Secrets Manager, Azure Key Vault, HashiCorp Vault, or Google Secret Manager.

See [Security Best Practices](/guides/security) for code samples covering each of these services, `.gitignore` patterns, and key masking in logs.

## Troubleshooting

### 401 Unauthorized

```json
{
  "status": 401,
  "title": "Unauthorized",
  "detail": "Invalid access token or API key"
}
```

**Solution**: Verify that your API key is correct, has not been revoked, and has not expired. Also confirm the `Authorization` header is formatted as `Bearer YOUR_API_KEY`, with a single space after `Bearer`.

### 403 Forbidden

Your API key is valid, but the account it belongs to lacks permission for the requested operation, or the API requires a license your organization does not have.

**Solution**: Check your licenses, verify you are accessing resources within your own organization, and contact support if you need additional permissions.

See [HTTP Status Codes](/guides/status-code) for the full list of response codes.

## Next Steps

- [Quick Start Guide](/guides/quickstart)
- [Best Practices](/guides/security)
- [API Reference](/api-reference)
