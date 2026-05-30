

# RBAC

## Overview

RBAC (Role-Based Access Control) is the Kubernetes authorization mechanism used to control who can perform actions on cluster resources.

RBAC helps enforce the principle of least privilege by granting only the permissions required to perform specific tasks.

---

## Why RBAC Matters

Without RBAC:

```text
User Access
      ↓
Unlimited Permissions
      ↓
Security Risk
```

With RBAC:

```text
User
 ↓
Role
 ↓
Allowed Actions
 ↓
Kubernetes Resources
```

Benefits:

- Improved Security
- Least Privilege Access
- Better Governance
- Compliance Support

---

## Core Components

### Role

Defines permissions within a namespace.

Examples:

```text
Read Pods
Create Deployments
View Services
```

---

### ClusterRole

Defines permissions across the cluster.

Examples:

```text
Manage Nodes
View All Namespaces
Cluster Administration
```

---

### RoleBinding

Associates a Role with a user, group, or Service Account.

---

### ClusterRoleBinding

Associates a ClusterRole with a user, group, or Service Account.

---

## RBAC Architecture

```text
User / Service Account
          ↓
      Role
          ↓
   RoleBinding
          ↓
 Kubernetes API
```

---

## Authorization Flow

```text
Request Sent
      ↓
Authentication
      ↓
RBAC Evaluation
      ↓
Permission Granted?
      ↓
Yes → Allow
No  → Deny
```

---

## Role vs ClusterRole

| Role | ClusterRole |
| ------ | ----------- |
| Namespace Scoped | Cluster Scoped |
| Limited Scope | Global Scope |
| Application Teams | Cluster Administrators |
| Safer By Default | Higher Privilege |

---

## Common Use Cases

### Developer Access

```text
View Pods
View Logs
Create Deployments
```

---

### Read-Only Access

```text
View Resources
No Modifications Allowed
```

---

### Cluster Administration

```text
Manage Entire Cluster
```

---

### Service Accounts

```text
Application
      ↓
Limited Kubernetes API Access
```

---

## Real Production Example

```text
Developer Team
        ↓
Role
        ↓
Read Pods
Read Logs
Deploy Applications
        ↓
Production Namespace
```

Benefits:

- Controlled Access
- Reduced Security Risk
- Better Auditability

---

## RBAC vs Authentication

| Authentication | RBAC |
| -------------- | ---- |
| Who Are You? | What Can You Do? |
| Identity Verification | Authorization |
| User Validation | Permission Validation |
| Login Focused | Access Focused |

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Forbidden Errors
- Missing RoleBindings
- Incorrect ClusterRoles
- Service Account Permission Issues
- Excessive Privileges

---

## Most Asked Interview Questions

1. What is RBAC?
2. Why is RBAC needed?
3. Role vs ClusterRole?
4. RoleBinding vs ClusterRoleBinding?
5. Authentication vs Authorization?
6. How does RBAC improve security?
7. How are Service Accounts used with RBAC?
8. What is least privilege access?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- RBAC controls Kubernetes authorization.
- Roles are namespace scoped.
- ClusterRoles are cluster scoped.
- RoleBindings assign permissions.
- Follow least privilege principles.
- One of the most important Kubernetes security topics.