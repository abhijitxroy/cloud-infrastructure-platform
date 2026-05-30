

# Secret

## Overview

A Secret is a Kubernetes object used to store sensitive information.

Secrets help prevent sensitive data from being hardcoded into:

- Application Code
- Container Images
- Configuration Files

Examples:

- Passwords
- API Keys
- Access Tokens
- Certificates
- Database Credentials

---

## Why Secrets Matter

Without Secrets:

```text
Credentials
      ↓
Stored In Code
      ↓
Security Risk
```

With Secrets:

```text
Credentials
      ↓
Secret
      ↓
Application
```

Benefits:

- Better Security
- Centralized Credential Management
- Reduced Exposure Risk
- Easier Rotation

---

## Architecture

```text
Secret
   ↓
Deployment
   ↓
Pod
   ↓
Application
```

Applications access Secrets at runtime.

---

## Common Use Cases

### Database Credentials

Examples:

```text
DB_USERNAME
DB_PASSWORD
```

---

### API Keys

Examples:

```text
PAYMENT_API_KEY
EMAIL_API_KEY
```

---

### Certificates

Examples:

```text
TLS Certificates
SSL Certificates
```

---

### Access Tokens

Examples:

```text
OAuth Tokens
Service Tokens
```

---

## How Applications Consume Secrets

### Environment Variables

```text
Secret
   ↓
Environment Variable
   ↓
Application
```

---

### Mounted Files

```text
Secret
   ↓
Volume Mount
   ↓
Application
```

---

## Secret vs ConfigMap

| Secret | ConfigMap |
| -------- | --------- |
| Sensitive Data | Non-Sensitive Data |
| Passwords | Application Settings |
| API Keys | Feature Flags |
| Certificates | Configuration Files |

---

## Security Considerations

Important:

```text
Base64 Encoding
≠
Encryption
```

Production Recommendations:

- Enable Encryption At Rest
- Use RBAC
- Rotate Credentials Regularly
- Follow Least Privilege Principles

---

## Real Production Example

```text
Spring Boot Application
          ↓
Secret
          ↓
DATABASE_PASSWORD
JWT_SECRET
API_KEY
```

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Missing Secrets
- Incorrect Secret Names
- Access Permission Issues
- Credential Rotation Problems
- Application Startup Failures

---

## Most Asked Interview Questions

1. What is a Kubernetes Secret?
2. Why are Secrets needed?
3. Secret vs ConfigMap?
4. How do Pods consume Secrets?
5. Are Secrets encrypted by default?
6. What sensitive data belongs in Secrets?
7. How should Secrets be secured?
8. What is encryption at rest?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Secrets store sensitive data.
- Secrets should be used for credentials and keys.
- Applications consume Secrets through environment variables or mounted files.
- Secrets are different from ConfigMaps.
- Base64 encoding is not encryption.
- Frequently asked Kubernetes security topic.