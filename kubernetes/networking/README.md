

# Networking

## Overview

Kubernetes networking enables communication between Pods, Services, Nodes, and external clients.

The networking model is designed to provide:

- Pod Connectivity
- Service Discovery
- Traffic Routing
- Load Balancing
- Network Security

Networking is a foundational part of every Kubernetes deployment.

---

## Why Networking Matters

Kubernetes applications depend on networking for:

- Service Communication
- Microservice Connectivity
- External Access
- Traffic Distribution
- Security Controls

Without networking, applications cannot communicate.

---

## Topics

- CNI (Container Network Interface)
- Service Networking
- Network Policy

---

## Networking Model

```text
Pod
 ↓
Service
 ↓
Cluster Network
 ↓
Other Pods
```

Kubernetes networking enables:

- Pod-to-Pod Communication
- Pod-to-Service Communication
- External-to-Service Communication

---

## Core Components

### CNI

Provides:

- IP Allocation
- Pod Networking
- Network Routing

### Service Networking

Provides:

- Stable Endpoints
- Service Discovery
- Load Balancing

### Network Policy

Provides:

- Traffic Control
- Pod Isolation
- Security Enforcement

---

## Learning Path

```text
Pod Networking
      ↓
CNI
      ↓
Services
      ↓
Service Discovery
      ↓
Network Policies
      ↓
Production Networking
```

---

## Related Sections

- Fundamentals
- Architecture
- Objects
- Security
- Operations

---

## Most Asked Interview Questions

1. How does Kubernetes networking work?
2. What is CNI?
3. How do Pods communicate?
4. What is Service Networking?
5. What is a Network Policy?
6. How is traffic routed inside a cluster?
7. Calico vs Cilium?
8. How do you secure Pod communication?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ High Priority

### Remember

- Kubernetes networking enables Pod communication.
- CNI provides cluster networking.
- Services provide stable access to Pods.
- Network Policies improve security.
- Networking is critical for production Kubernetes deployments.