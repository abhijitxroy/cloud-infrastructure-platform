

# Service Networking

## Overview

Service Networking provides stable network access to Kubernetes workloads.

Pods are ephemeral and can be created, deleted, or rescheduled at any time.

Services provide a stable endpoint that applications can use to communicate reliably.

Without Services:

```text
Application
      ↓
Direct Pod Access
      ↓
Pod Recreated
      ↓
Connection Breaks
```

With Services:

```text
Application
      ↓
Service
      ↓
Pods
```

---

## Why Service Networking Matters

Services provide:

- Stable Network Endpoints
- Service Discovery
- Load Balancing
- Pod Abstraction
- Reliable Communication

---

## Service Communication Model

```text
Client
   ↓
Service
   ↓
Pod A
Pod B
Pod C
```

The Service automatically distributes traffic.

---

## How Service Networking Works

### Step 1

Pods are created.

```text
Pod A
Pod B
Pod C
```

---

### Step 2

Service selects Pods using labels.

Example:

```text
app=frontend
```

---

### Step 3

Clients communicate with the Service.

```text
frontend-service
```

instead of individual Pods.

---

## Service Discovery

Kubernetes provides built-in DNS.

Example:

```text
frontend-service
backend-service
```

Applications communicate using service names.

---

## Load Balancing

A Service distributes traffic across matching Pods.

Example:

```text
Request 1 → Pod A
Request 2 → Pod B
Request 3 → Pod C
```

Benefits:

- Scalability
- Reliability
- Fault Tolerance

---

## Common Service Types

### ClusterIP

Default service type.

```text
Internal Cluster Access
```

---

### NodePort

```text
External Access Through Node Port
```

---

### LoadBalancer

```text
Cloud Provider Load Balancer
```

---

### ExternalName

```text
Maps Service To External DNS
```

---

## Real Production Example

```text
Frontend Service
        ↓
Frontend Pods

Backend Service
        ↓
Backend Pods

Database Service
        ↓
Database Pods
```

Benefits:

- Stable Connectivity
- Service Discovery
- Traffic Distribution

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Service Not Reachable
- Incorrect Label Selectors
- DNS Resolution Failures
- Endpoint Mismatches
- Load Balancing Issues

---

## Most Asked Interview Questions

1. What is Service Networking?
2. Why are Services needed?
3. How does a Service find Pods?
4. What is Service Discovery?
5. What is ClusterIP?
6. What is NodePort?
7. What is LoadBalancer?
8. How does Kubernetes load balancing work?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Services provide stable access to Pods.
- Services use labels to find Pods.
- Services support service discovery.
- Services provide load balancing.
- ClusterIP is the default service type.
- Service Networking is fundamental to Kubernetes.