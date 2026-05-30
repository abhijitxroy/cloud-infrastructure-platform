

# Shared Responsibility Model

## Overview

The AWS Shared Responsibility Model defines how security and operational responsibilities are divided between AWS and customers.

AWS is responsible for securing the cloud infrastructure, while customers are responsible for securing their applications, identities, operating systems, configurations, and data.

Understanding this model is essential for building secure and compliant AWS environments.

---

## Why It Matters

A common misconception is that AWS manages all security.

In reality:

```text
AWS
 ↓
Security Of The Cloud

Customer
 ↓
Security In The Cloud
```

Both AWS and customers have security responsibilities.

---

## AWS Responsibilities

AWS is responsible for:

- Physical Data Centers
- Hardware Infrastructure
- Storage Infrastructure
- Networking Infrastructure
- Global Infrastructure
- Availability Zones
- Regions
- Managed Service Infrastructure

```text
Physical Security
        ↓
AWS Responsibility
```

---

## Customer Responsibilities

Customers are responsible for:

- IAM Configuration
- User Access Management
- Security Groups
- Network Configuration
- Operating System Security
- Application Security
- Data Protection
- Encryption Configuration
- Compliance Requirements

```text
Applications
      ↓
Customer Responsibility
```

---

## Example: EC2

AWS Manages:

- Physical Servers
- Networking Hardware
- Storage Hardware
- Hypervisor

Customer Manages:

- Operating System
- Security Patches
- Installed Software
- Firewall Rules
- Application Security
- Data Protection

---

## Example: RDS

AWS Manages:

- Database Infrastructure
- Hardware
- Operating System Patching
- Availability

Customer Manages:

- Database Users
- Database Configuration
- Data Protection
- Access Controls

---

## Example: S3

AWS Manages:

- Storage Infrastructure
- Durability
- Availability

Customer Manages:

- Bucket Permissions
- Encryption Settings
- Access Controls
- Data Classification

---

## Managed Services Impact

Generally:

```text
More Managed Service
          ↓
Less Customer Responsibility
```

Example:

```text
EC2
 ↓
More Customer Management

RDS
 ↓
Less Customer Management
```

---

## Common Security Mistakes

- Excessive IAM Permissions
- Public S3 Buckets
- Missing Encryption
- Weak Access Controls
- Unpatched Systems

---

## Real Production Example

```text
AWS
 ↓
Infrastructure Security

Customer
 ↓
Identity Management
 ↓
Application Security
 ↓
Data Protection
```

Both parties contribute to overall security.

---

## Production Engineering Perspective

### Common Challenges

- IAM Misconfiguration
- Excessive Permissions
- Missing MFA
- Public Resources
- Incomplete Security Reviews

---

## Most Asked Questions

1. What is the Shared Responsibility Model?
2. What does AWS secure?
3. What must customers secure?
4. Who manages EC2 operating systems?
5. Who manages IAM?
6. Who manages S3 permissions?
7. Why is the model important?
8. How does responsibility change across services?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- AWS secures the cloud.
- Customers secure what runs in the cloud.
- IAM is always a customer responsibility.
- Data protection remains a customer responsibility.
- Responsibility varies by service type.
- One of the most important AWS security concepts.