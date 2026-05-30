# DNS

## Overview

DNS (Domain Name System) in Kubernetes provides service discovery for workloads running inside a cluster.

Applications communicate using Service names instead of Pod IP addresses.

This allows workloads to remain functional even when Pods are recreated and IP addresses change.

---

## Why DNS Matters

Without DNS:

```text
Application
      ↓
Pod IP Address
      ↓
Pod Recreated
      ↓
IP Changes
      ↓
Communication Breaks
```

With DNS:

```text
Application
      ↓
Service Name
      ↓
Kubernetes DNS
      ↓
Target Service
```

Benefits:

- Service Discovery
- Stable Connectivity
- Simplified Configuration
- Better Scalability

---

## Architecture

```text
Application A
       ↓
Kubernetes DNS
       ↓
Service
       ↓
Pods
```

DNS resolves service names into reachable service endpoints.

---

## How DNS Works

### Step 1

A Service is created.

```text
frontend-service
```

---

### Step 2

Kubernetes DNS creates DNS records.

---

### Step 3

Applications query the service name.

```text
frontend-service
```

---

### Step 4

DNS resolves the request to the Service.

---

## Common Use Cases

### Microservices

```text
Frontend
    ↓
backend-service
```

---

### Internal APIs

```text
Application
     ↓
user-service
```

---

### Database Access

```text
Application
     ↓
database-service
```

---

## DNS Components

Common Kubernetes DNS implementations:

- CoreDNS
- kube-dns (legacy)

CoreDNS is the standard DNS solution in modern Kubernetes clusters.

---

## Real Production Example

```text
Frontend Service
        ↓
API Service
        ↓
Database Service
```

Applications communicate using service names rather than IP addresses.

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- DNS Resolution Failures
- Service Not Found Errors
- CoreDNS Issues
- Incorrect Service Names
- Network Connectivity Problems

---

## Most Asked Interview Questions

1. What is Kubernetes DNS?
2. Why is DNS important in Kubernetes?
3. How does service discovery work?
4. What is CoreDNS?
5. How do applications find Services?
6. Why not use Pod IP addresses directly?
7. How are DNS records created?
8. How do you troubleshoot DNS issues?

---

## Quick Revision

### Priority

⭐⭐⭐⭐ High Priority

### Remember

- DNS provides service discovery.
- Applications communicate using Service names.
- CoreDNS is the default Kubernetes DNS solution.
- DNS removes dependency on Pod IP addresses.
- DNS is fundamental for microservice communication.