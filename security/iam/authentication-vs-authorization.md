

# Authentication vs Authorization

## Overview

Authentication and Authorization are two fundamental security concepts used to control access to systems, applications, infrastructure, and data.

Although often used together, they solve different problems.

Authentication verifies identity, while Authorization determines what actions an authenticated user or system is allowed to perform.

These concepts are heavily used in cloud platforms, Kubernetes, enterprise applications, CI/CD systems, and modern security architectures.

---

## Why Authentication And Authorization Matter

Without Authentication And Authorization:

```text
Users
   ↓
Unverified Access
   ↓
Security Risks
   ↓
Unauthorized Actions
```

With Authentication And Authorization:

```text
Users
   ↓
Authentication
   ↓
Verified Identity
   ↓
Authorization
   ↓
Controlled Access
```

Benefits:

- Improved Security
- Controlled Resource Access
- Better Governance
- Reduced Security Risk
- Regulatory Compliance

---

## Authentication

Authentication verifies identity.

Answers:

```text
Who are you?
```

Authentication occurs before authorization.

Common Methods:

- Username And Password
- Multi-Factor Authentication (MFA)
- Single Sign-On (SSO)
- Certificates
- Biometrics

Examples:

- Login To AWS Console
- Login To Kubernetes Dashboard
- Login To Enterprise Application

---

## Authorization

Authorization determines allowed actions.

Answers:

```text
What can you do?
```

Authorization occurs after successful authentication.

Examples:

- Read Access
- Write Access
- Delete Access
- Administrative Access
- Resource Management

---

## How Authentication And Authorization Work

```text
User
   ↓
Authentication
   ↓
Identity Verified
   ↓
Authorization
   ↓
Permission Evaluation
   ↓
Access Granted
```

---

## Common Authorization Models

### Role-Based Access Control (RBAC)

Permissions are assigned to roles.

Examples:

- Developer
- Administrator
- Auditor
- Read-Only User

---

### Attribute-Based Access Control (ABAC)

Access decisions are based on attributes.

Examples:

- Department
- Environment
- Resource Type
- Location

---

## Authentication vs Authorization

| Feature | Authentication | Authorization |
|----------|----------|----------|
| Purpose | Verify Identity | Determine Permissions |
| Question | Who Are You? | What Can You Do? |
| Happens First | Yes | No |
| Example | Login | Access Control |
| Result | Verified User | Allowed Actions |

---

## Production Usage

Authentication and Authorization are commonly used for:

- AWS IAM
- Kubernetes RBAC
- CI/CD Platforms
- Enterprise Applications
- Cloud Infrastructure
- Platform Engineering

---

## Production Engineering Perspective

### Common Challenges

- Weak Password Policies
- Missing MFA
- Excessive Permissions
- Privilege Escalation
- Misconfigured Roles

---

## Most Asked Questions

1. Authentication vs Authorization?
2. Which happens first?
3. What is MFA?
4. What is RBAC?
5. What is ABAC?
6. Why is least privilege important?
7. How does AWS IAM use these concepts?
8. How does Kubernetes RBAC work?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Where Used

- AWS IAM
- Kubernetes RBAC
- Azure AD
- CI/CD Platforms
- Enterprise Applications

### Remember

- Authentication verifies identity.
- Authorization determines permissions.
- Authentication happens first.
- MFA strengthens authentication.
- RBAC is widely used in cloud platforms.
- One of the most frequently asked security interview topics.