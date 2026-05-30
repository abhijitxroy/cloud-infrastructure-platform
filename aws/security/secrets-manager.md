

# Secrets Manager

## Overview

AWS Secrets Manager is a managed service used to securely store, retrieve, and manage sensitive information such as passwords, API keys, database credentials, and tokens.

It helps organizations eliminate hardcoded secrets and improve application security through centralized secret management.

---

## Why Secrets Manager Matters

```text
Credentials
     ↓
Hardcoded In Code
     ↓
Security Risk
```

With Secrets Manager:

```text
Credentials
     ↓
Secrets Manager
     ↓
Secure Access
```

Benefits:

- Centralized Secret Storage
- Improved Security
- Secret Rotation
- Access Control
- Reduced Credential Exposure

---

## How Secrets Manager Works

```text
Application
      ↓
Secrets Manager
      ↓
Secret Retrieval
      ↓
Secure Authentication
```

Applications retrieve secrets when needed instead of storing them in source code.

---

## What Can Be Stored

Examples:

- Database Credentials
- API Keys
- Access Tokens
- Application Secrets
- Third-Party Credentials

---

## Core Features

### Secure Storage

Secrets are encrypted and protected.

Commonly integrated with:

- KMS
- IAM
- AWS Applications

---

### Access Control

Access is controlled through IAM policies.

```text
User / Application
         ↓
IAM Policy
         ↓
Secret Access
```

---

### Secret Rotation

Secrets can be rotated automatically.

Benefits:

- Improved Security
- Reduced Credential Exposure
- Better Compliance

---

## Common Production Architecture

```text
Application
      ↓
Secrets Manager
      ↓
Database Credentials
      ↓
Database Access
```

---

## Secrets Manager vs Parameter Store

| Feature | Secrets Manager | Parameter Store |
|----------|----------------|----------------|
| Secret Storage | Yes | Yes |
| Automatic Rotation | Yes | Limited |
| Database Credential Management | Yes | Limited |
| Sensitive Data Focus | Yes | Partial |
| Managed Secret Lifecycle | Yes | Limited |

---

## Real Production Example

```text
Application
      ↓
Retrieve Database Password
      ↓
Secrets Manager
      ↓
Database Connection
```

Benefits:

- No Hardcoded Credentials
- Better Security
- Easier Credential Management

---

## Security Best Practices

- Never Hardcode Secrets
- Enable Secret Rotation
- Use Least Privilege Access
- Audit Secret Usage
- Encrypt Sensitive Information

---

## Production Engineering Perspective

### Common Challenges

- Hardcoded Credentials
- Excessive Secret Access
- Missing Rotation Policies
- Secret Lifecycle Management
- Compliance Requirements

---

## Most Asked Questions

1. What is AWS Secrets Manager?
2. Why use Secrets Manager?
3. What types of secrets can be stored?
4. How does secret rotation work?
5. Secrets Manager vs Parameter Store?
6. How is access controlled?
7. Why should secrets not be hardcoded?
8. How does Secrets Manager improve security?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Secrets Manager stores sensitive credentials securely.
- Secrets should never be hardcoded.
- IAM controls access to secrets.
- Secret Rotation improves security.
- Commonly used for database credentials and API keys.
- Core AWS security service.