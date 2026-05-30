

# Network Policies

## Overview

Network Policies are Kubernetes resources used to control network communication between Pods and other network endpoints.

They act as a Kubernetes firewall for Pod traffic and help enforce network segmentation inside a cluster.

Network Policies are a critical component of Kubernetes security.

---

## Why Network Policies Matter

Without Network Policies:

```text
Any Pod
    ↓
Can Communicate
    ↓
With Any Pod
```

With Network Policies:

```text
Allowed Traffic
       ↓
Explicit Rules
       ↓
Controlled Communication
```

Benefits:

- Reduced Attack Surface
- Better Security
- Network Isolation
- Compliance Support

---

## How Network Policies Work

Network Policies define:

- Allowed Ingress Traffic
- Allowed Egress Traffic

Traffic not explicitly allowed can be blocked.

---

## Network Policy Architecture

```text
Pod A
  ↓
Network Policy
  ↓
Pod B
```

The policy determines whether communication is permitted.

---

## Types of Rules

### Ingress Rules

Control incoming traffic.

```text
Who Can Access This Pod?
```

Examples:

- Frontend → Backend
- Application → Database

---

### Egress Rules

Control outgoing traffic.

```text
Where Can This Pod Connect?
```

Examples:

- Application → Database
- Application → External API

---

## Default Behavior

Without Network Policies:

```text
Allow All Traffic
```

After restrictive policies are applied:

```text
Only Explicitly Allowed Traffic
```

---

## Common Use Cases

### Frontend and Backend Isolation

```text
Frontend Pods
      ↓
Backend Pods
```

Only approved communication is allowed.

---

### Database Protection

```text
Application Pods
        ↓
Database Pods
```

Direct access from unrelated Pods is blocked.

---

### Multi-Tenant Clusters

```text
Team A Pods
     ✕
Team B Pods
```

Traffic isolation improves security.

---

## Network Policies vs RBAC

| Network Policies | RBAC |
| ---------------- | ---- |
| Controls Network Access | Controls API Access |
| Pod Communication | User Permissions |
| Network Security | Authorization |
| Traffic Focused | Identity Focused |

---

## Real Production Example

```text
Frontend
    ↓
Backend
    ↓
Database
```

Network Policies ensure:

```text
Frontend Cannot Access Database Directly
```

Benefits:

- Better Security
- Reduced Risk
- Controlled Communication

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Blocked Application Traffic
- DNS Connectivity Problems
- Incorrect Selectors
- Missing Egress Rules
- CNI Compatibility Issues

---

## Most Asked Interview Questions

1. What are Network Policies?
2. Why are Network Policies needed?
3. Ingress vs Egress Rules?
4. How do Network Policies improve security?
5. Network Policies vs RBAC?
6. What happens if no policy exists?
7. Why is traffic unexpectedly blocked?
8. How do microservices use Network Policies?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Network Policies control Pod communication.
- Ingress controls incoming traffic.
- Egress controls outgoing traffic.
- Policies improve workload isolation.
- Essential for zero-trust networking.
- Core Kubernetes security topic.