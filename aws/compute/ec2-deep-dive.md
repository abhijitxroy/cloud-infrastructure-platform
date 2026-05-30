

# EC2 Deep Dive

## Overview

Amazon Elastic Compute Cloud (EC2) is AWS's virtual machine service that provides scalable compute capacity in the cloud.

EC2 allows engineers to deploy applications without managing physical servers while maintaining control over operating systems, networking, storage, and security.

EC2 is one of the most widely used AWS services.

---

## Why EC2 Matters

Without EC2:

```text
Buy Hardware
      ↓
Install Servers
      ↓
Manage Datacenter
```

With EC2:

```text
Launch Instance
       ↓
Deploy Application
       ↓
Scale As Needed
```

Benefits:

- Elastic Capacity
- Faster Deployment
- Global Availability
- Pay-As-You-Go Pricing

---

## EC2 Architecture

```text
AWS Region
      ↓
Availability Zone
      ↓
EC2 Instance
      ↓
Application
```

---

## Core Components

### AMI (Amazon Machine Image)

An AMI is a template used to launch EC2 instances.

Examples:

- Amazon Linux
- Ubuntu
- Red Hat Enterprise Linux
- Windows Server

---

### Instance Type

Defines:

- CPU
- Memory
- Storage Performance
- Network Performance

Examples:

- General Purpose
- Compute Optimized
- Memory Optimized
- Storage Optimized

---

### Security Group

Acts as a virtual firewall.

Controls:

- Inbound Traffic
- Outbound Traffic

---

### EBS Volume

Provides persistent storage for EC2 instances.

---

## EC2 Lifecycle

```text
Launch
   ↓
Running
   ↓
Stopped
   ↓
Terminated
```

---

## Common Production Architecture

```text
Users
  ↓
Load Balancer
  ↓
EC2 Instances
  ↓
Database
```

---

## Scaling EC2

Common approaches:

### Vertical Scaling

```text
Small Instance
      ↓
Larger Instance
```

---

### Horizontal Scaling

```text
1 Instance
    ↓
Multiple Instances
```

Typically combined with:

- Auto Scaling
- Load Balancers

---

## EC2 Pricing Models

### On-Demand

Pay only for usage.

---

### Reserved Instances

Lower cost for long-term commitments.

---

### Spot Instances

Uses spare AWS capacity at reduced cost.

---

## Real Production Example

```text
Web Application
      ↓
Application Load Balancer
      ↓
Auto Scaling Group
      ↓
EC2 Instances
      ↓
RDS Database
```

Benefits:

- High Availability
- Fault Tolerance
- Scalability

---

## Production Engineering Perspective

### Common Challenges

- Incorrect Instance Sizing
- Security Group Misconfiguration
- Cost Optimization
- Storage Bottlenecks
- Scaling Limitations

---

## Most Asked Questions

1. What is EC2?
2. What is an AMI?
3. What is an Instance Type?
4. What is a Security Group?
5. EC2 vs Physical Servers?
6. Vertical vs Horizontal Scaling?
7. What is an EBS Volume?
8. How does EC2 achieve scalability?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- EC2 is AWS's virtual machine service.
- AMIs are templates used to launch instances.
- Instance Types define compute resources.
- Security Groups control network access.
- EBS provides persistent storage.
- Auto Scaling and Load Balancers are commonly used with EC2.