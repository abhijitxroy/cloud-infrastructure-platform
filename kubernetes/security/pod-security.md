

# Pod Security

## Overview

Pod Security focuses on protecting containers and workloads running inside Kubernetes Pods.

It helps reduce security risks by restricting dangerous container capabilities and enforcing secure runtime configurations.

Pod Security is a critical part of Kubernetes cluster hardening.

---

## Why Pod Security Matters

Without Pod Security:

```text
Container Compromise
         ↓
Node Compromise
         ↓
Cluster Risk
```

With Pod Security:

```text
Restricted Permissions
         ↓
Reduced Attack Surface
         ↓
Improved Security
```

Benefits:

- Reduced Security Risk
- Better Isolation
- Least Privilege Access
- Compliance Support

---

## Common Security Risks

### Privileged Containers

```text
Container
     ↓
Root-Level Access
     ↓
Host Risk
```

---

### Running As Root

```text
Application
      ↓
Root User
      ↓
Higher Security Risk
```

---

### Host Access

Examples:

- Host Network
- Host PID
- Host IPC

These increase exposure to the underlying node.

---

## Pod Security Standards

### Privileged

Least restrictive.

Allows advanced capabilities.

Suitable only for trusted infrastructure workloads.

---

### Baseline

Prevents common privilege escalation risks.

Provides a reasonable default security posture.

---

### Restricted

Most secure profile.

Enforces:

- Non-Root Containers
- Restricted Capabilities
- Limited Privileges

Recommended for production workloads.

---

## Security Best Practices

### Run As Non-Root

```text
Avoid Running Containers As Root
```

---

### Read-Only Filesystem

```text
Prevent Runtime File Changes
```

---

### Drop Unnecessary Capabilities

```text
Least Privilege Principle
```

---

### Avoid Privileged Containers

Use only when absolutely required.

---

### Restrict Host Access

Avoid:

- hostNetwork
- hostPID
- hostIPC

unless there is a strong operational requirement.

---

## Real Production Example

```text
Application Pod
      ↓
Non-Root User
      ↓
Restricted Profile
      ↓
Read-Only Filesystem
```

Benefits:

- Reduced Attack Surface
- Better Compliance
- Stronger Isolation

---

## Pod Security vs RBAC

| Pod Security | RBAC |
| ------------ | ---- |
| Secures Workloads | Secures Access |
| Container Focused | User Focused |
| Runtime Protection | Authorization Control |
| Pod Configuration | API Permissions |

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Privileged Container Restrictions
- Security Policy Violations
- Permission Denied Errors
- Non-Root Compatibility Issues
- Volume Access Problems

---

## Most Asked Interview Questions

1. What is Pod Security?
2. Why should containers avoid running as root?
3. What are Pod Security Standards?
4. Baseline vs Restricted profile?
5. What is a privileged container?
6. Why is least privilege important?
7. Pod Security vs RBAC?
8. How do you secure Pods in production?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Pod Security protects workloads.
- Avoid privileged containers.
- Run containers as non-root users.
- Use Restricted profile for production.
- Limit capabilities and host access.
- Core Kubernetes security topic.