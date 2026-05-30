

# Security

## Overview

AWS Security services help organizations protect identities, data, applications, and cloud infrastructure.

Security is a shared responsibility between AWS and customers and is a foundational requirement for operating production workloads in the cloud.

---

## Why Security Matters

Without Security Controls:

```text
Applications
      ↓
Data Exposure
      ↓
Security Risk
```

With Security Controls:

```text
Applications
      ↓
Identity Controls
Encryption
Secrets Protection
      ↓
Secure Environment
```

Benefits:

- Data Protection
- Access Control
- Compliance Support
- Risk Reduction
- Security Governance

---

## Topics Covered

### KMS

Focus Areas:

- Encryption
- Key Management
- Data Protection
- Key Rotation
- Compliance

---

### Secrets Manager

Focus Areas:

- Secret Storage
- Credential Management
- Secret Rotation
- Application Security
- Access Control

---

## Learning Path

```text
KMS
 ↓
Encryption
 ↓
Data Protection

Secrets Manager
 ↓
Credential Protection
 ↓
Application Security
```

---

## Common Production Architecture

```text
Application
      ↓
Secrets Manager
      ↓
Database Credentials

Application
      ↓
KMS
      ↓
Encrypted Data
```

---

## Real World Usage

AWS Security services are commonly used for:

- Application Security
- Database Security
- Encryption Management
- Compliance Requirements
- Secret Management
- Enterprise Governance

---

## Most Asked Questions

1. What is AWS KMS?
2. What is AWS Secrets Manager?
3. Why is encryption important?
4. What is key rotation?
5. How should secrets be stored?
6. KMS vs Secrets Manager?
7. How do applications securely access credentials?
8. What are common AWS security best practices?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- KMS manages encryption keys.
- Secrets Manager stores sensitive credentials.
- Encryption protects data at rest and in transit.
- Secrets should never be hardcoded.
- Security is a core cloud engineering responsibility.
- KMS and Secrets Manager are foundational AWS security services.