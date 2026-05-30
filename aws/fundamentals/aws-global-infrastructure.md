# AWS Global Infrastructure

## Overview

AWS Global Infrastructure is the worldwide network of data centers, regions, availability zones, and edge locations that power AWS services.

It enables organizations to deploy applications globally while achieving high availability, fault tolerance, low latency, and scalability.

Understanding AWS Global Infrastructure is fundamental to designing reliable cloud architectures.

---

## Why AWS Global Infrastructure Matters

Without Global Infrastructure:

```text
Single Datacenter
       ↓
Single Failure Point
       ↓
Reduced Availability
```

With AWS Global Infrastructure:

```text
Multiple Regions
       ↓
Multiple Availability Zones
       ↓
High Availability
```

Benefits:

- Global Reach
- Fault Tolerance
- Disaster Recovery
- Low Latency
- High Availability

---

## Core Components

### Region

A Region is a geographic area containing multiple Availability Zones.

Examples:

- us-east-1
- us-west-2
- eu-west-1
- ap-south-1

Characteristics:

- Independent Location
- Multiple Availability Zones
- Regional Service Deployment

---

### Availability Zone (AZ)

An Availability Zone consists of one or more data centers within a Region.

```text
Region
   ↓
AZ-A
AZ-B
AZ-C
```

Benefits:

- Fault Isolation
- High Availability
- Redundancy

---

### Edge Location

Edge Locations are global sites used for content delivery and low-latency services.

Commonly used by:

- CloudFront
- Route 53
- Global Accelerator

Benefits:

- Faster Content Delivery
- Reduced Latency
- Better User Experience

---

## Regional vs Global Services

### Regional Services

Examples:

- EC2
- RDS
- VPC
- EKS

Resources are deployed within a specific AWS Region.

---

### Global Services

Examples:

- IAM
- Route 53
- CloudFront

Available across AWS globally.

---

## High Availability Design

Typical production architecture:

```text
Region
  ↓
AZ-A
AZ-B
AZ-C
```

Applications are distributed across multiple Availability Zones.

Benefits:

- Improved Availability
- Reduced Downtime
- Better Resilience

---

## Disaster Recovery

Common strategy:

```text
Primary Region
       ↓
Secondary Region
```

Benefits:

- Business Continuity
- Regional Failure Protection
- Faster Recovery

---

## Real Production Example

```text
Users
  ↓
AWS Region
  ↓
Multiple AZs
  ↓
Application
```

Benefits:

- High Availability
- Fault Tolerance
- Scalability

---

## Production Engineering Perspective

### Common Challenges

- Single AZ Deployments
- Poor Region Selection
- Disaster Recovery Planning
- Cross-Region Costs
- Latency Optimization

---

## Most Asked Questions

1. What is an AWS Region?
2. What is an Availability Zone?
3. Region vs Availability Zone?
4. What are Edge Locations?
5. What are Global Services?
6. What are Regional Services?
7. Why deploy across multiple AZs?
8. How does AWS achieve high availability?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Regions contain multiple Availability Zones.
- Availability Zones provide fault isolation.
- Edge Locations reduce latency.
- EC2, RDS, and VPC are regional services.
- IAM and Route 53 are global services.
- Multi-AZ deployment is a core AWS best practice.
