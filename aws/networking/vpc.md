

# VPC

## Overview

Amazon Virtual Private Cloud (VPC) is a logically isolated virtual network within AWS.

A VPC enables organizations to launch AWS resources in a secure, controlled, and customizable network environment.

VPC is the foundation of AWS networking and is used by services such as EC2, RDS, Load Balancers, and many others.

---

## Why VPC Matters

Without VPC:

```text
Shared Network
      ↓
Limited Control
      ↓
Security Risks
```

With VPC:

```text
Custom Network
       ↓
Network Isolation
       ↓
Secure Resources
```

Benefits:

- Network Isolation
- Security Control
- Traffic Management
- Scalability
- Flexible Architecture

---

## How VPC Works

```text
AWS Region
      ↓
VPC
      ↓
Subnets
      ↓
AWS Resources
```

Resources are deployed inside subnets that belong to a VPC.

---

## Core Components

### CIDR Block

A CIDR block defines the IP address range available within a VPC.

Example:

```text
10.0.0.0/16
```

This range can be divided into multiple subnets.

---

### Subnets

Subnets divide a VPC into smaller network segments.

Types:

- Public Subnet
- Private Subnet

---

### Route Tables

Route Tables control how network traffic flows inside and outside the VPC.

---

### Security Groups

Security Groups act as virtual firewalls protecting AWS resources.

---

## Public And Private Architecture

```text
Internet
   ↓
Public Subnet
   ↓
Load Balancer

Private Subnet
   ↓
Application Servers
   ↓
Database
```

This is one of the most common production architectures.

---

## VPC Benefits

### Isolation

Resources are separated from other AWS customers.

---

### Security

Access is controlled through:

- Security Groups
- Route Tables
- Subnets

---

### Scalability

Supports applications ranging from small deployments to large enterprise platforms.

---

## Common Production Architecture

```text
VPC
 ↓
Public Subnet
 ↓
Load Balancer

Private Subnet
 ↓
Application Servers
 ↓
Database
```

Benefits:

- High Availability
- Security
- Scalability
- Better Isolation

---

## Real Production Example

```text
Users
  ↓
Load Balancer
  ↓
Application Tier
  ↓
Database Tier
```

All resources operate inside a VPC.

---

## Production Engineering Perspective

### Common Challenges

- Poor CIDR Planning
- Overlapping Networks
- Misconfigured Routing
- Security Misconfiguration
- Limited IP Capacity

---

## Most Asked Questions

1. What is a VPC?
2. Why is a VPC required?
3. What is a CIDR Block?
4. What are Public and Private Subnets?
5. What services run inside a VPC?
6. How does VPC improve security?
7. What is the relationship between VPC and Subnets?
8. Why is VPC considered the foundation of AWS networking?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- VPC is a logically isolated AWS network.
- VPC is the foundation of AWS networking.
- CIDR blocks define available IP ranges.
- Subnets divide a VPC into smaller networks.
- Security Groups and Route Tables control traffic.
- Most AWS architectures start with a VPC.