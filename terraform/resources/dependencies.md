

# Dependencies

## Overview

Dependencies define relationships between Terraform resources and determine the order in which infrastructure is created, updated, or destroyed.

Terraform uses dependency information to build a dependency graph and safely manage infrastructure changes.

Understanding dependencies is critical for reliable infrastructure provisioning and avoiding deployment failures.

---

## Why Dependencies Matter

Without Dependencies:

```text
Resource Creation
        ↓
Incorrect Order
        ↓
Deployment Failure
```

With Dependencies:

```text
Dependency Graph
        ↓
Correct Order
        ↓
Successful Deployment
```

Benefits:

- Reliable Provisioning
- Correct Resource Order
- Reduced Failures
- Better Infrastructure Management

---

## Dependency Graph

Terraform automatically builds:

```text
Dependency Graph
```

Example:

```text
VPC
 ↓
Subnet
 ↓
EC2 Instance
```

Resources are created in the required order.

---

## Types of Dependencies

### Implicit Dependencies

Created automatically when one resource references another.

Example Flow:

```text
VPC
 ↓
Subnet
 ↓
Instance
```

Terraform detects the relationship automatically.

---

### Explicit Dependencies

Defined when Terraform cannot automatically determine the relationship.

Used when:

- External Dependencies Exist
- Operational Ordering Is Required
- Resources Must Wait For Other Actions

---

## Resource Creation Flow

```text
Network
    ↓
Compute
    ↓
Application
```

Dependencies ensure resources are provisioned safely.

---

## Resource Destruction Flow

Terraform reverses dependency order.

Example:

```text
Application
    ↓
Compute
    ↓
Network
```

This prevents resource conflicts.

---

## Common Dependency Examples

### Networking Dependencies

```text
VPC
 ↓
Subnet
 ↓
Security Group
```

---

### Kubernetes Dependencies

```text
VPC
 ↓
EKS Cluster
 ↓
Node Groups
```

---

### Database Dependencies

```text
Network
 ↓
Database
 ↓
Application
```

---

## Common Problems

### Circular Dependencies

Example:

```text
A Depends On B
B Depends On A
```

Results in deployment failures.

---

### Hidden Dependencies

Can create:

- Unexpected Failures
- Resource Ordering Issues

---

### Manual Infrastructure Changes

Can break dependency assumptions.

---

## Real Production Example

```text
VPC
 ↓
Subnets
 ↓
Load Balancer
 ↓
Kubernetes Cluster
 ↓
Applications
```

Terraform manages provisioning order automatically.

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Circular Dependencies
- Missing References
- Incorrect Resource Ordering
- Infrastructure Drift
- Deployment Failures

---

## Most Asked Interview Questions

1. What are Terraform dependencies?
2. Why are dependencies important?
3. What is a dependency graph?
4. Implicit vs Explicit dependencies?
5. What are circular dependencies?
6. How does Terraform determine resource order?
7. Why can dependency issues cause failures?
8. How are dependencies handled during resource deletion?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Dependencies determine resource order.
- Terraform builds a dependency graph.
- Implicit dependencies are preferred.
- Explicit dependencies are used when needed.
- Circular dependencies cause failures.
- Core Terraform resource-management concept.