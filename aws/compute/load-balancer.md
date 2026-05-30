

# Load Balancer

## Overview

A Load Balancer distributes incoming traffic across multiple servers or application instances.

In AWS, Load Balancers improve availability, scalability, fault tolerance, and application reliability by preventing traffic from being directed to a single server.

Load Balancers are commonly used with EC2 instances, Auto Scaling Groups, and container platforms.

---

## Why Load Balancers Matter

Without Load Balancer:

```text
Users
  ↓
Single Server
  ↓
Single Point Of Failure
```

With Load Balancer:

```text
Users
  ↓
Load Balancer
  ↓
Multiple Servers
```

Benefits:

- High Availability
- Fault Tolerance
- Scalability
- Better Performance

---

## How Load Balancing Works

```text
Client Requests
       ↓
Load Balancer
       ↓
Target Instances
```

Traffic is distributed across healthy targets.

---

## Common AWS Load Balancers

### Application Load Balancer (ALB)

Best For:

- HTTP Applications
- HTTPS Applications
- Microservices
- Container Platforms

Features:

- Layer 7 Routing
- Path-Based Routing
- Host-Based Routing

---

### Network Load Balancer (NLB)

Best For:

- High Performance Applications
- TCP Traffic
- Low Latency Workloads

Features:

- Layer 4 Routing
- High Throughput
- Static IP Support

---

### Gateway Load Balancer (GWLB)

Best For:

- Security Appliances
- Network Inspection
- Traffic Filtering

---

## Health Checks

Load Balancers continuously verify target health.

```text
Healthy Instance
        ↓
Receives Traffic

Unhealthy Instance
        ↓
Removed From Rotation
```

Benefits:

- Improved Reliability
- Automatic Failure Handling

---

## Load Balancer and Auto Scaling

Common architecture:

```text
Users
  ↓
Load Balancer
  ↓
Auto Scaling Group
  ↓
EC2 Instances
```

Benefits:

- Elastic Capacity
- High Availability
- Fault Tolerance

---

## Traffic Distribution

Examples:

- Round Robin Style Distribution
- Multiple Availability Zones
- Cross-Zone Traffic Distribution

---

## Real Production Example

```text
Users
  ↓
Application Load Balancer
  ↓
Web Tier
  ↓
Application Tier
  ↓
Database Tier
```

Benefits:

- Better Availability
- Scalable Architecture
- Improved User Experience

---

## Production Engineering Perspective

### Common Challenges

- Incorrect Health Checks
- Unbalanced Traffic
- SSL Configuration Issues
- Target Registration Problems
- Availability Zone Misconfiguration

---

## Most Asked Questions

1. What is a Load Balancer?
2. Why use a Load Balancer?
3. What is an Application Load Balancer?
4. What is a Network Load Balancer?
5. How do Health Checks work?
6. Why combine Load Balancers with Auto Scaling?
7. How does a Load Balancer improve availability?
8. ALB vs NLB?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Load Balancers distribute traffic across targets.
- ALB operates at Layer 7.
- NLB operates at Layer 4.
- Health Checks remove unhealthy instances.
- Commonly used with Auto Scaling Groups.
- Core AWS scalability and availability concept.