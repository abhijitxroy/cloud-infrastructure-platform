# Secrets Management

## Overview

Secrets Management is the process of securely storing, accessing, and managing sensitive information in Kubernetes.

Secrets allow applications to use confidential data without hardcoding credentials into source code, container images, or configuration files.

Examples of secrets include passwords, API keys, certificates, and tokens.

---

## Why Secrets Management Matters

Without Secrets Management:

```text
Credentials In Source Code
          ↓
Security Risk
          ↓
Potential Data Breach
```

With Secrets Management:

```text
Sensitive Data
       ↓
Kubernetes Secret
       ↓
Controlled Access
       ↓
Application
```

Benefits:

- Improved Security
- Credential Protection
- Better Compliance
- Reduced Operational Risk

---

## What Is a Secret?

A Secret is a Kubernetes object used to store sensitive information.

Examples:

- Database Passwords
- API Keys
- TLS Certificates
- Access Tokens
- SSH Keys

---

## Secret Architecture

```text
Application
      ↓
Pod
      ↓
Secret
      ↓
Sensitive Data
```

Applications consume Secrets securely at runtime.

---

## How Secrets Work

### Step 1

Secret is created.

---

### Step 2

Pod references the Secret.

---

### Step 3

Kubernetes makes the Secret available.

---

### Step 4

Application accesses the Secret.

---

## Common Secret Types

### Opaque

General-purpose secret.

Examples:

```text
Passwords
API Keys
```

---

### TLS Secret

Stores:

```text
Certificates
Private Keys
```

---

### Docker Registry Secret

Stores:

```text
Container Registry Credentials
```

---

## Secret Consumption Methods

### Environment Variables

```text
Secret
   ↓
Environment Variable
   ↓
Application
```

---

### Mounted Volumes

```text
Secret
   ↓
Mounted File
   ↓
Application
```

Commonly preferred for certificates and keys.

---

## Security Best Practices

### Follow Least Privilege

Only authorized workloads should access secrets.

---

### Avoid Hardcoding Credentials

Never store secrets inside:

- Source Code
- Git Repositories
- Container Images

---

### Rotate Secrets Regularly

Reduce long-term credential exposure.

---

### Restrict RBAC Access

Limit who can read or modify secrets.

---

### Use External Secret Stores

Examples:

- HashiCorp Vault
- AWS Secrets Manager
- Azure Key Vault
- Google Secret Manager

---

## Secrets vs ConfigMaps

| Secrets | ConfigMaps |
| -------- | ---------- |
| Sensitive Data | Non-Sensitive Configuration |
| Credentials | Application Settings |
| Restricted Access | General Access |
| Security Focused | Configuration Focused |

---

## Real Production Example

```text
Application
      ↓
Database Password
      ↓
Kubernetes Secret
      ↓
Database Connection
```

Benefits:

- Secure Credential Storage
- Better Access Control
- Reduced Security Risk

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Missing Secrets
- Incorrect Secret Names
- RBAC Permission Issues
- Application Startup Failures
- Secret Rotation Problems

---

## Most Asked Interview Questions

1. What is a Kubernetes Secret?
2. Why are Secrets needed?
3. Secrets vs ConfigMaps?
4. How do Pods consume Secrets?
5. Why should credentials not be hardcoded?
6. How should Secrets be secured?
7. What external secret managers are commonly used?
8. How does RBAC protect Secrets?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Secrets store sensitive information.
- Avoid hardcoding credentials.
- Secrets can be mounted or exposed as environment variables.
- Restrict access using RBAC.
- Rotate secrets regularly.
- Core Kubernetes security topic.
