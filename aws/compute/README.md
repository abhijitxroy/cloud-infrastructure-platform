

# Compute

## Overview

AWS Compute services provide processing power required to run applications, services, workloads, and platforms in the cloud.

Compute services are responsible for executing application logic, handling user requests, running business workloads, and supporting scalable architectures.

Compute is one of the core pillars of AWS infrastructure.

---

## Why Compute Matters

Without Compute:

```text
Application Code
        ↓
Cannot Execute
```

With Compute:

```text
Application Code
        ↓
Compute Resources
        ↓
Running Application
```

Benefits:

- Scalability
- Flexibility
- High Availability
- Faster Deployment
- Reduced Infrastructure Management

---

## Topics Covered

### EC2 Deep Dive

Focus Areas:

- Virtual Machines
- Instance Types
- AMIs
- Security Groups
- Storage Integration

---

### Load Balancer

Focus Areas:

- Traffic Distribution
- High Availability
- Health Checks
- Fault Tolerance

---

### Auto Scaling

Focus Areas:

- Automatic Scaling
- Capacity Management
- Availability
- Cost Optimization

---

## Learning Path

```text
EC2
 ↓
Load Balancer
 ↓
Auto Scaling
 ↓
Scalable Architecture
```

---

## Common Production Architecture

```text
Users
  ↓
Load Balancer
  ↓
Auto Scaling Group
  ↓
EC2 Instances
  ↓
Database
```

Benefits:

- High Availability
- Elastic Capacity
- Fault Tolerance

---

## Real World Usage

AWS Compute services are commonly used for:

- Web Applications
- APIs
- Enterprise Applications
- Microservices
- Platform Services
- Internal Tools

---

## Most Asked Questions

1. What is AWS Compute?
2. What is EC2?
3. Why use Load Balancers?
4. What is Auto Scaling?
5. Vertical vs Horizontal Scaling?
6. How does AWS achieve high availability?
7. Why combine Load Balancers with Auto Scaling?
8. How do teams scale applications on AWS?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- EC2 provides virtual machines.
- Load Balancers distribute traffic.
- Auto Scaling adjusts capacity automatically.
- Compute is the foundation of application hosting.
- Load Balancer + Auto Scaling is a common production pattern.
- Core AWS infrastructure domain.