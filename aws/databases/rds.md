

# Amazon RDS

## Overview

Amazon Relational Database Service (RDS) is AWS's managed relational database service.

RDS simplifies database administration by automating infrastructure provisioning, backups, patching, monitoring, and high availability.

It allows teams to focus on application development instead of database infrastructure management.

---

## Why RDS Matters

Without RDS:

```text
Provision Servers
        ↓
Install Database
        ↓
Manage Backups
        ↓
Manage Availability
```

With RDS:

```text
Create Database
       ↓
AWS Manages Operations
       ↓
Application Uses Database
```

Benefits:

- Reduced Operational Overhead
- Automated Backups
- High Availability
- Easier Scaling
- Improved Reliability

---

## How RDS Works

```text
Application
      ↓
RDS Instance
      ↓
Stored Data
```

AWS manages the underlying infrastructure while users manage database configuration and data.

---

## Supported Database Engines

Examples:

- MySQL
- PostgreSQL
- MariaDB
- Oracle
- Microsoft SQL Server

---

## Core Components

### DB Instance

A managed database server running inside AWS.

Responsibilities:

- Query Processing
- Data Storage
- Connection Handling

---

### Storage

Persistent storage used by the database.

Characteristics:

- Durable
- Scalable
- Managed By AWS

---

### Endpoint

Applications connect to RDS using an endpoint.

```text
Application
      ↓
RDS Endpoint
      ↓
Database
```

---

## High Availability

### Multi-AZ Deployment

RDS can maintain a standby database in another Availability Zone.

```text
Primary Database
        ↓
Replication
        ↓
Standby Database
```

Benefits:

- Fault Tolerance
- Improved Availability
- Automatic Failover

---

## Backup and Recovery

Features:

- Automated Backups
- Manual Snapshots
- Point-In-Time Recovery

---

## Scaling Options

### Vertical Scaling

```text
Small Instance
      ↓
Larger Instance
```

---

### Storage Scaling

Increase storage capacity as data grows.

---

## RDS vs DynamoDB

| Feature | RDS | DynamoDB |
|----------|----------|----------|
| Database Type | Relational | NoSQL |
| Schema | Structured | Flexible |
| Queries | SQL | Key Based Access |
| Scaling | Managed | Automatic |
| Best For | Transactional Systems | Large Scale Applications |

---

## Common Use Cases

- E-Commerce Applications
- Enterprise Applications
- Content Management Systems
- Financial Applications
- Internal Business Systems

---

## Real Production Example

```text
Users
  ↓
Web Application
  ↓
RDS Database
  ↓
Business Data
```

Benefits:

- Reliable Storage
- Managed Operations
- High Availability

---

## Production Engineering Perspective

### Common Challenges

- Poor Query Performance
- Incorrect Instance Sizing
- Cost Optimization
- Connection Management
- Backup Planning

---

## Most Asked Questions

1. What is Amazon RDS?
2. Why use RDS instead of self-managed databases?
3. What database engines does RDS support?
4. What is Multi-AZ?
5. How does RDS improve availability?
6. RDS vs DynamoDB?
7. What are RDS Snapshots?
8. How does RDS simplify database management?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- RDS is a managed relational database service.
- Supports MySQL, PostgreSQL, Oracle, SQL Server, and MariaDB.
- Multi-AZ improves availability.
- Automated backups simplify recovery.
- Applications connect using database endpoints.
- Common choice for transactional workloads.