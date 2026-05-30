# DynamoDB

## Overview

Amazon DynamoDB is AWS's fully managed NoSQL database service.

It is designed to provide high performance, low latency, automatic scaling, and high availability without requiring infrastructure management.

DynamoDB is commonly used for internet-scale applications that require predictable performance and massive scalability.

---

## Why DynamoDB Matters

Traditional Databases:

```text
Manage Servers
       ↓
Manage Scaling
       ↓
Manage Availability
```

DynamoDB:

```text
Create Table
      ↓
Store Data
      ↓
Automatic Scaling
```

Benefits:

- Fully Managed
- Low Latency
- High Scalability
- High Availability
- Reduced Operational Overhead

---

## How DynamoDB Works

```text
Application
      ↓
DynamoDB Table
      ↓
Stored Data
```

Data is stored in tables and accessed using keys.

---

## Core Concepts

### Table

A table is the primary container for data.

Examples:

- Users
- Orders
- Products
- Sessions

---

### Item

An item represents a single record in a table.

Equivalent to a row in relational databases.

---

### Attribute

An attribute represents a data field.

Examples:

- UserID
- Email
- OrderID
- Status

---

### Primary Key

Used to uniquely identify items.

Types:

- Partition Key
- Partition Key + Sort Key

---

## DynamoDB Architecture

```text
Application
      ↓
Partition Key
      ↓
DynamoDB Partitions
      ↓
Stored Data
```

Data distribution is handled automatically.

---

## Common Features

### Automatic Scaling

DynamoDB automatically adjusts capacity based on workload demand.

---

### High Availability

Data is replicated across multiple Availability Zones.

---

### Backup and Recovery

Supports:

- Backups
- Point-In-Time Recovery

---

### Global Tables

Supports multi-region replication for global applications.

---

## DynamoDB vs RDS

| Feature | DynamoDB | RDS |
|----------|----------|-----|
| Database Type | NoSQL | Relational |
| Scaling | Automatic | More Management Required |
| Schema | Flexible | Structured |
| Performance | Very High | Depends On Workload |
| Use Cases | Large Scale Applications | Transactional Systems |

---

## Common Use Cases

- User Profiles
- Shopping Carts
- Session Management
- Gaming Platforms
- IoT Applications
- Real-Time Applications

---

## Real Production Example

```text
Users
  ↓
Web Application
  ↓
DynamoDB
  ↓
User Profiles
Orders
Sessions
```

Benefits:

- Low Latency
- Massive Scale
- Operational Simplicity

---

## Production Engineering Perspective

### Common Challenges

- Poor Partition Key Design
- Hot Partitions
- Access Pattern Mistakes
- Cost Optimization
- Data Modeling Complexity

---

## Most Asked Questions

1. What is DynamoDB?
2. Is DynamoDB SQL or NoSQL?
3. What is a Partition Key?
4. DynamoDB vs RDS?
5. How does DynamoDB scale?
6. What are Global Tables?
7. What are common DynamoDB use cases?
8. Why is DynamoDB considered serverless?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- DynamoDB is a fully managed NoSQL database.
- Tables contain items and attributes.
- Primary Keys uniquely identify data.
- DynamoDB scales automatically.
- Global Tables support multi-region deployments.
- Commonly used for large-scale low-latency applications.
