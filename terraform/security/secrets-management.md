

# Secrets Management

## Overview

Secrets Management is the practice of securely storing, accessing, rotating, and protecting sensitive credentials used by Terraform.

Examples include:

- API Keys
- Cloud Credentials
- Database Passwords
- Tokens
- Certificates

Improper secret handling can expose infrastructure and create significant security risks.

---

## Why Secrets Management Matters

Without Secrets Management:

```text
Credentials
      ↓
Exposed In Code
      ↓
Security Incident
```

With Secrets Management:

```text
Secure Secret Storage
          ↓
Controlled Access
          ↓
Protected Infrastructure
```

Benefits:

- Better Security
- Reduced Risk
- Improved Compliance
- Safer Automation

---

## Common Terraform Secrets

Examples:

- AWS Access Keys
- Azure Credentials
- GCP Credentials
- Database Passwords
- Kubernetes Tokens
- API Tokens

---

## Why Hardcoding Secrets Is Dangerous

Avoid storing secrets in:

```text
Terraform Files
Git Repositories
Configuration Files
```

Risks:

- Credential Exposure
- Unauthorized Access
- Compliance Violations

---

## Recommended Secret Sources

### Cloud Secret Managers

Examples:

- AWS Secrets Manager
- Azure Key Vault
- Google Secret Manager

---

### Dedicated Secret Platforms

Examples:

- HashiCorp Vault
- Enterprise Secret Management Systems

---

### CI/CD Secret Stores

Examples:

- Pipeline Secrets
- Deployment Credentials
- Environment Variables

---

## Secret Access Flow

```text
Terraform
     ↓
Secret Store
     ↓
Credential Retrieval
     ↓
Infrastructure Provisioning
```

---

## Secret Management Best Practices

### Follow Least Privilege

Grant only required access.

---

### Rotate Credentials Regularly

Benefits:

- Reduced Exposure
- Improved Security

---

### Centralize Secret Storage

Avoid multiple unmanaged copies.

---

### Audit Secret Access

Track:

- Who Accessed Secrets
- When Access Occurred
- What Was Used

---

### Avoid Plain Text Storage

Never expose secrets through:

- Source Code
- Documentation
- Shared Files

---

## Real Production Example

```text
Terraform Pipeline
        ↓
Vault
        ↓
Temporary Credentials
        ↓
AWS Infrastructure
```

Benefits:

- Reduced Credential Exposure
- Better Governance
- Improved Auditability

---

## Production Engineering Perspective

### Common Risks

- Hardcoded Credentials
- Secret Leakage
- Excessive Permissions
- Missing Rotation Policies
- State File Exposure

---

## Most Asked Interview Questions

1. What is Secrets Management?
2. Why should secrets never be hardcoded?
3. How should Terraform access secrets?
4. What are common secret storage solutions?
5. Why rotate credentials?
6. What is least privilege access?
7. How can secrets be exposed accidentally?
8. How do teams manage secrets securely?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Never hardcode secrets.
- Use centralized secret stores.
- Follow least privilege principles.
- Rotate credentials regularly.
- Audit secret access.
- Secrets management is a core Terraform security topic.