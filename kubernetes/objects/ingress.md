# Ingress

## Overview

Ingress is a Kubernetes resource used to manage external access to services running inside a cluster.

It provides routing capabilities that allow external traffic to reach application workloads through defined rules.

Ingress commonly works with HTTP and HTTPS traffic.

---

## Responsibilities

Common responsibilities:

- External traffic routing
- Path based routing
- Host based routing
- TLS termination
- Centralized traffic entry management

---

## Traffic Flow

Example workflow:

External Client

↓

Ingress

↓

Kubernetes Service

↓

Application Pods

Ingress provides a controlled entry point for traffic entering Kubernetes environments.

---

## Routing Examples

Examples:

- Route traffic based on application path
- Route traffic based on domain name
- Direct requests to different backend services

---

## Ingress and Egress

Ingress:

- Incoming traffic entering workloads

Egress:

- Outgoing traffic leaving workloads

These concepts are commonly used while designing communication patterns inside distributed systems.

---

## Notes

Ingress simplifies external application exposure and helps improve traffic management for Kubernetes based workloads.
# Ingress

## Overview

Ingress is a Kubernetes resource used to manage external access to services running inside a cluster.

It provides HTTP and HTTPS routing rules that allow external users to access Kubernetes applications through a single entry point.

Ingress helps avoid exposing every service individually.

---

## Why Ingress Matters

Without Ingress:

```text
Internet
   ↓
Service A

Internet
   ↓
Service B

Internet
   ↓
Service C
```

Multiple external endpoints are required.

With Ingress:

```text
Internet
    ↓
 Ingress
    ↓
Service A
Service B
Service C
```

Benefits:

- Centralized Traffic Management
- Reduced Cost
- Simplified Routing
- TLS Management
- Better Security

---

## Architecture

```text
External Client
        ↓
     Ingress
        ↓
      Service
        ↓
        Pods
```

Ingress routes traffic to Kubernetes Services.

Services route traffic to Pods.

---

## Responsibilities

### External Traffic Routing

Routes traffic from external users into the cluster.

---

### Host-Based Routing

Example:

```text
api.company.com
        ↓
API Service

app.company.com
        ↓
Frontend Service
```

---

### Path-Based Routing

Example:

```text
/api
   ↓
Backend Service

/web
   ↓
Frontend Service
```

---

### TLS Termination

Handles HTTPS certificates.

Benefits:

- Secure Communication
- Centralized Certificate Management

---

## Ingress Controller

Important:

```text
Ingress Resource
       ↓
Requires
       ↓
Ingress Controller
```

Popular Controllers:

- NGINX Ingress Controller
- Traefik
- HAProxy
- Cloud Provider Controllers

Without an Ingress Controller, Ingress resources do not process traffic.

---

## Real Production Example

```text
shop.company.com
         ↓
      Ingress
         ↓
Frontend Service
         ↓
Frontend Pods

api.company.com
         ↓
Backend Service
         ↓
Backend Pods
```

---

## Ingress vs LoadBalancer

| Ingress | LoadBalancer |
| -------- | ------------ |
| Layer 7 Routing | Layer 4 Routing |
| Host-Based Routing | No Host Routing |
| Path-Based Routing | No Path Routing |
| Multiple Services | Usually Single Service |
| Cost Efficient | More Expensive |

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- 404 Errors
- Incorrect Routing Rules
- TLS Certificate Problems
- DNS Misconfiguration
- Ingress Controller Failures

---

## Most Asked Interview Questions

1. What is Ingress?
2. Why is Ingress needed?
3. What is an Ingress Controller?
4. Host-based vs path-based routing?
5. Ingress vs LoadBalancer?
6. How does TLS termination work?
7. Can Ingress expose multiple services?
8. What happens if an Ingress Controller is missing?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Ingress manages external HTTP/HTTPS traffic.
- Ingress routes traffic to Services.
- Ingress requires an Ingress Controller.
- Supports host-based and path-based routing.
- Commonly used for production Kubernetes applications.
- Frequently asked Kubernetes interview topic.