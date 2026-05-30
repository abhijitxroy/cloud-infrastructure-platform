# Load Balancing Basics

## Overview

Load balancing distributes incoming traffic across multiple application instances or infrastructure resources.

It helps improve application availability, operational stability and resource utilization.

Load balancing becomes increasingly important as infrastructure environments scale and application demand changes over time.

---

## Common Objectives

Load balancing commonly supports:

- Traffic distribution
- High availability
- Fault tolerance
- Scalability
- Resource optimization

---

## Traffic Flow

Example workflow:

Client Request

↓

Load Balancer

↓

Application Instance 1

or

Application Instance 2

or

Application Instance 3

Traffic distribution helps prevent workloads from concentrating on a single infrastructure component.

---

## Common Load Balancing Models

### Layer 4 Load Balancing

Traffic routing based on transport layer information.

Examples:

- TCP
- UDP

---

### Layer 7 Load Balancing

Traffic routing based on application layer information.

Examples:

- HTTP routing
- URL path routing
- Host based routing

---

## Operational Benefits

Load balancing helps improve:

- Application availability
- Infrastructure resilience
- Traffic management
- Operational flexibility

---

## Common Infrastructure Usage

Examples:

- Cloud platforms
- Kubernetes environments
- Web applications
- API infrastructure

---

## Notes

Load balancing plays an important role in distributed systems where workload demand, resilience and scalability requirements evolve over time.
# Load Balancing Basics

## Overview

Load Balancing is the process of distributing incoming network or application traffic across multiple servers, services, containers, or infrastructure resources.

Load balancing improves availability, scalability, performance, and fault tolerance by preventing traffic from overwhelming a single system.

Load balancing is a critical component of cloud platforms, Kubernetes environments, microservices architectures, and large-scale distributed systems.

---

## Why Load Balancing Matters

Without Load Balancing:

```text
Users
   ↓
Single Server
   ↓
Performance Bottleneck
   ↓
Potential Failure
```

With Load Balancing:

```text
Users
   ↓
Load Balancer
   ↓
Server 1
Server 2
Server 3
```

Benefits:

- High Availability
- Scalability
- Fault Tolerance
- Better Performance
- Efficient Resource Utilization

---

## How Load Balancing Works

```text
Client Requests
       ↓
Load Balancer
       ↓
Backend Services
       ↓
Response
```

The load balancer receives traffic and distributes requests across healthy backend systems.

---

## Common Load Balancing Types

### Layer 4 Load Balancing

Traffic routing based on network and transport layer information.

Examples:

- TCP
- UDP
- IP Address
- Port Number

---

### Layer 7 Load Balancing

Traffic routing based on application layer information.

Examples:

- HTTP Routing
- HTTPS Routing
- URL Path Routing
- Host-Based Routing

---

## Load Balancing Algorithms

### Round Robin

Requests are distributed sequentially across servers.

---

### Least Connections

Traffic is sent to the server with the fewest active connections.

---

### Weighted Distribution

Traffic is distributed based on server capacity.

---

## Common Production Usage

Load balancing is commonly used for:

- Web Applications
- API Platforms
- Kubernetes Services
- Cloud Infrastructure
- Microservices Platforms
- High-Traffic Systems

---

## Cloud Examples

Examples:

- AWS Application Load Balancer (ALB)
- AWS Network Load Balancer (NLB)
- Kubernetes Ingress Controllers
- API Gateways

---

## Production Engineering Perspective

### Common Challenges

- Uneven Traffic Distribution
- Health Check Failures
- Session Management Issues
- Misconfigured Routing Rules
- Capacity Planning Problems

---

## Most Asked Questions

1. What is load balancing?
2. Why is load balancing important?
3. Layer 4 vs Layer 7 load balancing?
4. What is Round Robin?
5. What is Least Connections?
6. Why are health checks important?
7. How is load balancing used in Kubernetes?
8. How is load balancing used in cloud platforms?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Load balancing distributes traffic across systems.
- Improves availability and scalability.
- Layer 4 uses network information.
- Layer 7 uses application information.
- Essential for cloud and Kubernetes environments.
- Frequently asked networking interview topic.