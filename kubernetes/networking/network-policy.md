

# Network Policy

## Overview

A Network Policy is a Kubernetes resource used to control network traffic between Pods.

By default, Pods can communicate freely with other Pods inside the cluster.

Network Policies allow engineers to define:

- Allowed Traffic
- Denied Traffic
- Ingress Rules
- Egress Rules

They provide network-level security for Kubernetes workloads.

---

## Why Network Policies Matter

Without Network Policies:

```text
Pod A
  ↕
Pod B
  ↕
Pod C
```

All Pods may communicate.

With Network Policies:

```text
Pod A
  ↓
Allowed
  ↓
Pod B

Pod C
  ✕
Blocked
```

Benefits:

- Zero Trust Networking
- Better Security
- Traffic Isolation
- Compliance Requirements

---

## Ingress And Egress

### Ingress

Controls incoming traffic.

```text
External Source
       ↓
      Pod
```

---

### Egress

Controls outgoing traffic.

```text
Pod
 ↓
External Service
```

---

## Architecture Example

```text
Frontend Pod
      ↓
Allowed
      ↓
Backend Pod

Frontend Pod
      ✕
Blocked
      ✕
Database Pod
```

---

## Common Use Cases

### Application Isolation

Only allow required services to communicate.

---

### Database Protection

```text
Backend
   ↓
Database
```

Allowed.

```text
Frontend
   ↓
Database
```

Blocked.

---

### Namespace Isolation

Restrict communication between namespaces.

---

### Compliance Requirements

Limit access to sensitive workloads.

---

## Dependency On CNI

Important:

```text
Network Policies Require
CNI Support
```

Common Supported CNIs:

- Calico
- Cilium
- Weave Net

---

## Real Production Example

```text
Frontend Service
        ↓
Backend Service
        ↓
Database
```

Rules:

- Frontend → Backend Allowed
- Backend → Database Allowed
- Frontend → Database Blocked

Result:

```text
Reduced Attack Surface
```

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Pod Connectivity Failures
- Incorrect Label Selection
- CNI Limitations
- Missing Egress Rules
- Namespace Communication Issues

---

## Most Asked Interview Questions

1. What is a Network Policy?
2. Why are Network Policies needed?
3. What is Ingress traffic?
4. What is Egress traffic?
5. How do Network Policies improve security?
6. Do Network Policies work without CNI support?
7. Calico and Network Policies relationship?
8. How would you isolate database access?

---

## Quick Revision

### Priority

⭐⭐⭐⭐ High Priority

### Remember

- Network Policies control Pod traffic.
- They define ingress and egress rules.
- They improve Kubernetes security.
- Network Policies depend on CNI support.
- Commonly implemented using Calico or Cilium.
- Frequently asked Kubernetes networking interview topic.