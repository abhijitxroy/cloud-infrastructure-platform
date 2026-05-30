

# Databases

## Overview

AWS Database services provide managed solutions for storing, retrieving, processing, and managing application data.

Databases are a critical component of modern applications and support everything from transactional workloads to large-scale internet applications.

AWS offers both relational and NoSQL database services.

---

## Why Databases Matter

Without Databases:

```text
Application
      ↓
No Persistent Data
```

With Databases:

```text
Application
      ↓
Database
      ↓
Persistent Data
```

Benefits:

- Data Persistence
- Reliability
- Scalability
- High Availability
- Business Continuity

---

## Topics Covered

### Amazon RDS

Focus Areas:

- Relational Databases
- SQL Workloads
- Multi-AZ Deployments
- Backups And Recovery
- Managed Database Operations

---

### DynamoDB

Focus Areas:

- NoSQL Databases
- Massive Scale
- Automatic Scaling
- Low Latency
- Global Applications

---

## Learning Path

```text
RDS
 ↓
Relational Databases

DynamoDB
 ↓
NoSQL Databases
```

---

## Database Types

### Relational Databases

Examples:

- MySQL
- PostgreSQL
- Oracle
- SQL Server

Commonly used for:

- Business Applications
- Financial Systems
- ERP Platforms

---

### NoSQL Databases

Examples:

- DynamoDB

Commonly used for:

- Internet Scale Applications
- Session Management
- Gaming Platforms
- Real-Time Systems

---

## Common Production Architecture

```text
Users
  ↓
Application
  ↓
RDS / DynamoDB
  ↓
Business Data
```

---

## Real World Usage

AWS databases are commonly used for:

- E-Commerce Platforms
- Enterprise Applications
- SaaS Products
- Analytics Systems
- Mobile Applications
- Microservices Platforms

---

## Most Asked Questions

1. What database services does AWS provide?
2. What is Amazon RDS?
3. What is DynamoDB?
4. RDS vs DynamoDB?
5. SQL vs NoSQL?
6. When should DynamoDB be used?
7. When should RDS be used?
8. How does AWS improve database availability?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- RDS is a managed relational database service.
- DynamoDB is a managed NoSQL database service.
- RDS is best for transactional workloads.
- DynamoDB is best for massive scale and low latency.
- AWS manages infrastructure, backups, and availability.
- Databases are a core AWS infrastructure domain.