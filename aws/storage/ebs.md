

# EBS

## Overview

Amazon Elastic Block Store (EBS) is a block storage service designed for use with Amazon EC2 instances.

EBS provides persistent storage that remains available even if an EC2 instance is stopped or restarted.

It is commonly used for operating systems, databases, enterprise applications, and workloads requiring low-latency storage.

---

## Why EBS Matters

Without Persistent Storage:

```text
Instance Stops
      ↓
Data Loss Risk
```

With EBS:

```text
Instance Stops
      ↓
Data Remains Available
```

Benefits:

- Persistent Storage
- High Performance
- Low Latency
- Scalability
- Reliability

---

## How EBS Works

```text
EC2 Instance
      ↓
EBS Volume
      ↓
Stored Data
```

EBS volumes are attached to EC2 instances and behave like virtual hard drives.

---

## Core Components

### EBS Volume

A block storage device attached to an EC2 instance.

Examples:

- Operating System Disk
- Application Storage
- Database Storage

---

### Snapshot

A backup of an EBS volume stored in Amazon S3.

Benefits:

- Backup
- Disaster Recovery
- Data Migration

---

## Volume Types

### SSD Volumes

Best For:

- Databases
- Applications
- Boot Volumes

Characteristics:

- Low Latency
- High Performance

---

### HDD Volumes

Best For:

- Large Sequential Workloads
- Log Processing
- Data Warehousing

Characteristics:

- Lower Cost
- High Throughput

---

## Common Production Architecture

```text
Application
      ↓
EC2 Instance
      ↓
EBS Volume
```

---

## EBS vs S3

| Feature | EBS | S3 |
|----------|-----|----|
| Storage Type | Block Storage | Object Storage |
| Attachment | EC2 Instances | Independent Service |
| Latency | Low | Higher |
| Common Usage | Operating Systems, Databases | Files, Backups, Objects |
| File System Required | Yes | No |

---

## Real Production Example

```text
EC2 Instance
      ↓
Application
      ↓
EBS Volume
      ↓
Database Files
```

Benefits:

- Persistent Data
- Reliable Performance
- Fast Access

---

## Production Engineering Perspective

### Common Challenges

- Incorrect Volume Sizing
- Missing Backups
- Cost Optimization
- Performance Bottlenecks
- Snapshot Management

---

## Most Asked Questions

1. What is Amazon EBS?
2. Why is EBS used with EC2?
3. What is an EBS Snapshot?
4. EBS vs S3?
5. SSD vs HDD Volumes?
6. Does EBS persist after instance restart?
7. What workloads use EBS?
8. How does EBS improve application performance?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- EBS is AWS block storage.
- Commonly attached to EC2 instances.
- Data persists independently of instance restarts.
- Snapshots provide backup and recovery.
- SSD volumes are common for databases and applications.
- Core AWS storage service.