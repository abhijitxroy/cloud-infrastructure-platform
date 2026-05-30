# Service

## Overview

A Service is a Kubernetes object that provides a stable network endpoint for a group of Pods.

Pods are ephemeral and can be recreated at any time.

A Service provides a consistent way for applications to communicate with Pods without depending on Pod IP addresses.

---

## Why Services Matter

Without Services:

```text
Client
  ↓
Pod IP
  ↓
Pod Recreated
  ↓
IP Changes
  ↓
Connection Breaks
```

With Services:

```text
Client
  ↓
Service
  ↓
Pods
```

Benefits:

- Stable Networking
- Service Discovery
- Load Balancing
- Pod Abstraction
- Reliable Communication

---

## Architecture

```text
Client
   ↓
Service
   ↓
Pod A
Pod B
Pod C
```

The Service distributes traffic across matching Pods.

---

## How Services Work

### Step 1

Pods are created.

```text
Pod A
Pod B
Pod C
```

---

### Step 2

Pods receive labels.

Example:

```text
app=frontend
```

---

### Step 3

The Service selects Pods using label selectors.

```text
frontend-service
       ↓
app=frontend
```

---

### Step 4

Traffic is distributed across matching Pods.

---

## Service Types

### ClusterIP

Default service type.

```text
Internal Cluster Access
```

Use Cases:

- Backend Services
- Internal APIs

---

### NodePort

```text
External Access Through Worker Node Port
```

Use Cases:

- Testing
- Small Environments

---

### LoadBalancer

```text
Cloud Load Balancer
        ↓
Kubernetes Service
```

Use Cases:

- Production Applications
- Public Services

---

### ExternalName

```text
Service
    ↓
External DNS Name
```

Use Cases:

- External Databases
- Third Party Services

---

## Service Discovery

Kubernetes provides built-in DNS.

Applications communicate using service names.

Examples:

```text
frontend-service
backend-service
database-service
```

---

## Load Balancing

Example:

```text
Request 1 → Pod A
Request 2 → Pod B
Request 3 → Pod C
```

Benefits:

- Scalability
- High Availability
- Better Resource Utilization

---

## Service vs Ingress

| Service | Ingress |
| -------- | -------- |
| Internal Traffic Routing | External Traffic Routing |
| Pod Access | Service Access |
| Layer 4 Networking | Layer 7 Routing |
| Required For Applications | Optional Entry Layer |

---

## Real Production Example

```text
Internet
    ↓
Ingress
    ↓
Frontend Service
    ↓
Frontend Pods

Frontend Service
    ↓
Backend Service
    ↓
Backend Pods
```

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Service Not Reachable
- Incorrect Label Selectors
- Missing Endpoints
- DNS Resolution Problems
- Load Balancing Issues

---

## Most Asked Interview Questions

1. What is a Kubernetes Service?
2. Why are Services required?
3. How does a Service find Pods?
4. What is a label selector?
5. What is ClusterIP?
6. What is NodePort?
7. What is LoadBalancer?
8. Service vs Ingress?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Services provide stable access to Pods.
- Services use label selectors to find Pods.
- Services support service discovery.
- Services provide built-in load balancing.
- ClusterIP is the default service type.
- One of the most important Kubernetes interview topics.
