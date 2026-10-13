---
source: https://developer.extremeplatformone.com/content/guides/best-practices/security.md
---

---
title: "Security Best Practices"
---

Security is paramount when integrating with APIs. This guide covers best practices for securing your API keys, communications, and data.

## Store API Keys Securely

Never hardcode API keys in your source code:

```javascript
// ❌ Bad - Hardcoded key
const apiKey = 'extr_sk_v1...';

// ✅ Good - Environment variable
const apiKey = process.env.EXTREME_API_KEY;

// ✅ Better - Secrets manager
const apiKey = await secretsManager.getSecret('extreme-api-key');
```

## Environment Variables

Store sensitive configuration in environment variables:

```bash
# .env file (never commit this!)
EXTREME_API_KEY=your_api_key_here
EXTREME_API_BASE_URL=https://${API_DOMAIN}
```

```javascript
// Load environment variables
require('.env').config();

const apiClient = axios.create({
  baseURL: process.env.EXTREME_API_BASE_URL,
  headers: {
    'Authorization': `Bearer ${process.env.EXTREME_API_KEY}`
  }
});
```

### Protect .env Files

Add to `.gitignore`:

```gitignore
# Environment variables
.env
.env.local
.env.*.local

# API keys and secrets
*.key
*.pem
secrets.json
```

## Secrets Management

For production applications, use a secrets management service:

### AWS Secrets Manager

```javascript
const AWS = require('aws-sdk');
const secretsManager = new AWS.SecretsManager();

async function getApiKey() {
  const data = await secretsManager.getSecretValue({
    SecretId: 'extreme-api-key'
  }).promise();

  return JSON.parse(data.SecretString).apiKey;
}

const apiKey = await getApiKey();
```

### Azure Key Vault

```javascript
const { SecretClient } = require('@azure/keyvault-secrets');
const { DefaultAzureCredential } = require('@azure/identity');

const credential = new DefaultAzureCredential();
const client = new SecretClient(
  'https://your-vault.vault.azure.net',
  credential
);

const secret = await client.getSecret('extreme-api-key');
const apiKey = secret.value;
```

### HashiCorp Vault

```javascript
const vault = require('node-vault')({
  endpoint: 'https://vault.example.com',
  token: process.env.VAULT_TOKEN
});

const { data } = await vault.read('secret/data/extreme-api');
const apiKey = data.data.apiKey;
```

## Validate SSL Certificates

Don't disable SSL verification in production:

```javascript
// ❌ Bad - Disables SSL verification
const https = require('https');
const agent = new https.Agent({
  rejectUnauthorized: false
});

// ✅ Good - Use default SSL verification
const response = await axios.get(url); // Default is secure
```

## Rotate API Keys

- ✅ Rotate keys every 90 days
- ✅ Rotate immediately if compromised
- ✅ Maintain backup keys during rotation
- ✅ Document rotation procedures
- ✅ Test backup keys regularly

## Prevent Common Vulnerabilities

### Command Injection

```javascript
// ❌ Bad - Command injection vulnerability
const userId = req.query.userId;
exec(`curl https://${API_DOMAIN}/iam/v1/users/${userId}`);

// ✅ Good - Use parameterized requests
const userId = req.query.userId;
await apiClient.get(`https://${API_DOMAIN}/iam/v1/users/${encodeURIComponent(userId)}`);
```

## Secure API Key Transmission

### Never Log API Keys

```javascript
// ❌ Bad - Logs API key
console.log('Using API key:', apiKey);

// ✅ Good - Mask sensitive data
console.log('Using API key:', maskApiKey(apiKey));

function maskApiKey(key) {
  return key.slice(0, 10) + '...' + key.slice(-4);
}
```

## Next Steps

- [Error Handling](/guides/error-handling) - Handle errors securely
- [Authentication](/guides/authentication) - Learn about authentication methods
- [API Keys](/api-keys) - Manage your API keys
