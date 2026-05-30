

# Route Table

## Overview

A Route Table is a set of rules that determines how network traffic is routed within a VPC.

Route Tables control where traffic is sent, allowing resources to communicate with other resources inside the VPC, the internet, or external networks.

Every subnet in a VPC must be associated with a Route Table.

---

## Why Route Tables Matter

Without Route Tables:

```text
Network Traffic
       ↓
No Route
       ↓
Communication Failure
```

With Route Tables:

```text
Network Traffic
       ↓
Route Table
       ↓
Correct Destination
```

Benefits:

- Traffic Control
- Network Connectivity
- Internet Access
- Internal Communication
- Network Isolation

---

## How Route Tables Work

```text
Source Resource
        ↓
Route Table
        ↓
Destination
```

Each route contains a destination and a target.

---

## Route Components

### Destination

Defines where traffic should go.

Examples:

- VPC CIDR Block
- Internet CIDR (0.0.0.0/0)
- Private Network CIDR

---

### Target

Defines where traffic is forwarded.

Examples:

- Local Route
- Internet Gateway
- NAT Gateway
- Virtual Private Gateway

---

## Default Route Table

Every VPC includes a default Route Table.

Example:

```text
Destination
10.0.0.0/16
      ↓
Local
```

This allows communication between resources inside the VPC.

---

## Public Subnet Route Table

```text
Destination      Target
10.0.0.0/16      Local
0.0.0.0/0        Internet Gateway
```

Benefits:

- Internet Connectivity
- Public Access

---

## Private Subnet Route Table

```text
Destination      Target
10.0.0.0/16      Local
0.0.0.0/0        NAT Gateway
```

Benefits:

- Outbound Internet Access
- No Direct Public Exposure

---

## Common Production Architecture

```text
Internet
   ↓
Internet Gateway
   ↓
Public Subnet
   ↓
Load Balancer

Private Subnet
   ↓
Application Servers
```

Route Tables determine traffic flow between these components.

---

## Real Production Example

```text
User Request
      ↓
Load Balancer
      ↓
Application Server
      ↓
Database
```

Route Tables ensure traffic reaches the correct destination.

---

## Production Engineering Perspective

### Common Challenges

- Incorrect Routes
- Missing Internet Access
- Connectivity Issues
- Route Conflicts
- Private Subnet Misconfiguration

---

## Most Asked Questions

1. What is a Route Table?
2. Why is a Route Table required?
3. What is a route destination?
4. What is a route target?
5. Public vs Private Route Tables?
6. How does internet access work in AWS?
7. What is the default Route Table?
8. How are Route Tables associated with subnets?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Route Tables control network traffic flow.
- Every subnet uses a Route Table.
- Routes contain destinations and targets.
- Internet Gateway enables public internet access.
- NAT Gateway enables outbound access for private resources.
- Core AWS networking concept.