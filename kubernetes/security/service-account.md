

# Service Account

## Overview

A Service Account is a Kubernetes identity used by applications and workloads running inside a cluster.

While RBAC controls permissions, Service Accounts provide the identity that workloads use when interacting with the Kubernetes API.

Applications should use Service Accounts instead of user credentials.

---

## Why Service Accounts Matter

Without Service Accounts:

```text
Application
      ↓
User Credentials
      ↓
Security Risk
```

With Service Accounts:

```text
Application
      ↓
Service Account
      ↓
RBAC Permissions
      ↓
Kubernetes API
```

Benefits:

- Secure Workload Identity
- Least Privilege Access
- Better Auditing
- Improved Security

---

## How Service Accounts Work

Every Pod can be associated with a Service Account.

```text
Pod
 ↓
Service Account
 ↓
Authentication Token
 ↓
Kubernetes API
```

The Service Account identity is used whenever the workload communicates with the cluster.

---

## Authentication Flow

```text
Application
      ↓
Service Account Token
      ↓
API Server
      ↓
Authentication
      ↓
RBAC Authorization
```

---

## Default Service Account

Every namespace automatically contains:

```text
default
```

Service Account.

If no Service Account is specified:

```text
Pod Uses Default Service Account
```

Production Recommendation:

```text
Avoid Using Default Service Account
```

Create dedicated Service Accounts for workloads.

---

## Service Account and RBAC

Service Accounts are commonly combined with RBAC.

```text
Service Account
        ↓
Role
        ↓
RoleBinding
        ↓
Allowed Actions
```

Example:

```text
Read Pods
Read ConfigMaps
Read Services
```

---

## Common Use Cases

### Kubernetes Operators

```text
Operator
    ↓
Manage Resources
```

---

### CI/CD Pipelines

```text
Pipeline
    ↓
Deploy Applications
```

---

### Monitoring Systems

```text
Monitoring Tool
       ↓
Read Cluster State
```

---

### Application Integrations

```text
Application
      ↓
Access Kubernetes API
```

---

## Service Account vs User Account

| Service Account | User Account |
| --------------- | ------------ |
| Workload Identity | Human Identity |
| Used By Pods | Used By Users |
| Application Authentication | User Authentication |
| Automated Access | Interactive Access |

---

## Real Production Example

```text
Monitoring Application
         ↓
Service Account
         ↓
Read-Only RBAC Role
         ↓
Cluster Metrics
```

Benefits:

- Controlled Access
- Least Privilege
- Better Security

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Forbidden Errors
- Missing RoleBindings
- Incorrect Service Account Assignment
- Token Authentication Problems
- Excessive Permissions

---

## Most Asked Interview Questions

1. What is a Service Account?
2. Why are Service Accounts needed?
3. Service Account vs User Account?
4. How do Service Accounts work with RBAC?
5. Why avoid the default Service Account?
6. How do Pods authenticate to the API Server?
7. What permissions should Service Accounts have?
8. How do you secure workload access?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Service Accounts provide workload identity.
- Pods use Service Accounts to access the Kubernetes API.
- RBAC controls what Service Accounts can do.
- Avoid using the default Service Account in production.
- Follow least privilege principles.
- Core Kubernetes security topic.