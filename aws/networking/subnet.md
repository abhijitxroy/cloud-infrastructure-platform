

# Subnet

## Overview

A Subnet is a logical subdivision of a VPC that allows resources to be organized and isolated within a network.

Subnets help control traffic flow, improve security, and support scalable cloud architectures.

Every subnet exists within a single Availability Zone.

---

## Why Subnets Matter

Without Subnets:

```text
Single Network
      ↓
Limited Isolation
      ↓
Security Challenges
```

With Subnets:

```text
VPC
 ↓
Public Subnet
Private Subnet
```

Benefits:

- Network Segmentation
- Improved Security
- Better Traffic Control
- High Availability Design
- Easier Resource Management

---

## How Subnets Work

```text
VPC
 ↓
Subnet
 ↓
AWS Resources
```

Resources are deployed inside subnets.

Examples:

- EC2 Instances
- Load Balancers
- Databases

---

## Types of Subnets

### Public Subnet

A public subnet has a route to the Internet Gateway.

Common Resources:

- Load Balancers
- Bastion Hosts
- Public Web Servers

Example:

```text
Internet
   ↓
Internet Gateway
   ↓
Public Subnet
```

---

### Private Subnet

A private subnet does not allow direct internet access.

Common Resources:

- Application Servers
- Databases
- Internal Services

Example:

```text
Private Subnet
      ↓
Application Server
      ↓
Database
```

---

## Availability Zone Relationship

A subnet belongs to a single Availability Zone.

Example:

```text
Region
  ↓
AZ-A
 └─ Public Subnet

AZ-B
 └─ Private Subnet
```

Using multiple Availability Zones improves availability.

---

## Common Production Architecture

```text
Internet
   ↓
Load Balancer
   ↓
Public Subnet
   ↓
Application Servers
   ↓
Private Subnet
   ↓
Database
```

Benefits:

- Better Security
- High Availability
- Improved Isolation

---

## Public vs Private Subnet

| Feature | Public Subnet | Private Subnet |
|----------|--------------|---------------|
| Internet Access | Yes | No Direct Access |
| Common Usage | Load Balancers | Applications, Databases |
| Security Exposure | Higher | Lower |
| Typical Placement | Edge Layer | Internal Layer |

---

## Real Production Example

```text
Users
  ↓
Load Balancer
  ↓
Public Subnet
  ↓
Application Servers
  ↓
Private Subnet
  ↓
Database
```

This architecture is widely used in production AWS environments.

---

## Production Engineering Perspective

### Common Challenges

- Incorrect Subnet Design
- Public Exposure Of Internal Services
- Availability Zone Imbalance
- IP Address Planning Issues
- Network Segmentation Problems

---

## Most Asked Questions

1. What is a Subnet?
2. Why are Subnets required?
3. What is a Public Subnet?
4. What is a Private Subnet?
5. Public vs Private Subnet?
6. How are Subnets related to Availability Zones?
7. Why place databases in private subnets?
8. What is a common subnet architecture?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Subnets divide a VPC into smaller networks.
- Every subnet belongs to one Availability Zone.
- Public subnets have internet connectivity.
- Private subnets protect internal resources.
- Production architectures use both public and private subnets.
- Core AWS networking concept.