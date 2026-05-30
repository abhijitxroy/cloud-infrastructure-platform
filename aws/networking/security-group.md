

# Security Group

## Overview

A Security Group is a virtual firewall that controls inbound and outbound traffic for AWS resources.

Security Groups help protect EC2 instances, databases, load balancers, and other AWS services by allowing only approved network traffic.

Security Groups are one of the most important security controls in AWS.

---

## Why Security Groups Matter

Without Security Groups:

```text
Internet
    ↓
Unrestricted Access
    ↓
Security Risk
```

With Security Groups:

```text
Internet
    ↓
Security Group Rules
    ↓
Controlled Access
```

Benefits:

- Network Security
- Access Control
- Reduced Attack Surface
- Improved Compliance
- Resource Protection

---

## How Security Groups Work

```text
Network Traffic
       ↓
Security Group
       ↓
Allow Or Deny Access
```

Security Groups evaluate traffic based on configured rules.

---

## Core Concepts

### Inbound Rules

Control incoming traffic.

Examples:

- HTTP (80)
- HTTPS (443)
- SSH (22)
- Database Ports

---

### Outbound Rules

Control outgoing traffic.

Examples:

- Internet Access
- API Communication
- Database Connectivity

---

## Security Group Characteristics

### Stateful Firewall

Security Groups are stateful.

```text
Request Allowed
      ↓
Response Automatically Allowed
```

Return traffic does not require additional rules.

---

### Resource Level Security

Security Groups are attached directly to resources.

Examples:

- EC2 Instances
- Load Balancers
- RDS Databases

---

## Common Security Group Rules

### Web Server

```text
Port 80  → HTTP
Port 443 → HTTPS
```

---

### SSH Access

```text
Port 22 → SSH
```

Should be restricted to trusted sources.

---

### Database Access

```text
Port 3306 → MySQL
Port 5432 → PostgreSQL
```

Typically restricted to application servers.

---

## Common Production Architecture

```text
Internet
   ↓
Load Balancer
   ↓
Application Servers
   ↓
Database
```

Each layer uses dedicated Security Groups.

---

## Security Group Example

```text
Load Balancer SG
        ↓
Allow 80,443

Application SG
        ↓
Allow From Load Balancer

Database SG
        ↓
Allow From Application SG
```

Benefits:

- Layered Security
- Least Privilege Access
- Better Isolation

---

## Security Group vs NACL

| Feature | Security Group | NACL |
|----------|---------------|------|
| Scope | Resource Level | Subnet Level |
| Stateful | Yes | No |
| Allow Rules | Yes | Yes |
| Deny Rules | No | Yes |
| Common Usage | Resource Protection | Network Boundary Protection |

---

## Production Engineering Perspective

### Common Challenges

- Open SSH Access
- Excessive Permissions
- Unused Rules
- Poor Rule Management
- Security Misconfiguration

---

## Most Asked Questions

1. What is a Security Group?
2. Why are Security Groups important?
3. What are inbound rules?
4. What are outbound rules?
5. What does stateful mean?
6. Security Group vs NACL?
7. How should database access be configured?
8. What are Security Group best practices?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Security Groups act as virtual firewalls.
- They control inbound and outbound traffic.
- Security Groups are stateful.
- Applied directly to AWS resources.
- Commonly protect EC2, RDS, and Load Balancers.
- Core AWS networking and security concept.