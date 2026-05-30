

# Storage

## Overview

Kubernetes Storage provides persistent data management for applications running inside a cluster.

Unlike containers and Pods, storage can survive restarts, rescheduling, upgrades, and failures.

Storage is essential for stateful workloads that need to retain data.

---

## Why Storage Matters

Without Persistent Storage:

```text
Pod Deleted
     ↓
Data Lost
```

With Kubernetes Storage:

```text
Pod Deleted
     ↓
Data Preserved
     ↓
New Pod Uses Same Data
```

Benefits:

- Data Persistence
- Better Reliability
- Stateful Application Support
- Infrastructure Abstraction

---

## Topics

### Persistent Storage

- Persistent Volume (PV)
- Persistent Volume Claim (PVC)

### Dynamic Provisioning

- StorageClass

---

## Storage Architecture

```text
Application
      ↓
Pod
      ↓
PVC
      ↓
PV
      ↓
Storage Backend
```

Examples:

- AWS EBS
- Azure Disk
- Google Persistent Disk
- NFS
- Ceph

---

## Storage Workflow

```text
Application Requests Storage
             ↓
PVC Created
             ↓
StorageClass Selected
             ↓
PV Provisioned
             ↓
Storage Mounted To Pod
```

---

## Common Use Cases

### Databases

```text
MySQL
PostgreSQL
MongoDB
```

### Message Queues

```text
Kafka
RabbitMQ
```

### Search Platforms

```text
Elasticsearch
OpenSearch
```

### Stateful Applications

```text
Applications Requiring Persistent Data
```

---

## Storage Components

### Persistent Volume

Provides storage.

### Persistent Volume Claim

Requests storage.

### StorageClass

Automates storage provisioning.

---

## Real Production Example

```text
PostgreSQL StatefulSet
         ↓
PVC
         ↓
StorageClass
         ↓
Cloud Block Storage
```

Benefits:

- Persistent Data
- Automated Provisioning
- Better Reliability

---

## Related Sections

- Objects
- Operations
- Security
- StatefulSet

---

## Most Asked Interview Questions

1. Why is persistent storage needed?
2. What is a Persistent Volume?
3. What is a Persistent Volume Claim?
4. PV vs PVC?
5. What is a StorageClass?
6. What is dynamic provisioning?
7. Which workloads require persistent storage?
8. How does Kubernetes manage stateful data?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- PV provides storage.
- PVC requests storage.
- StorageClass enables dynamic provisioning.
- Storage survives Pod recreation.
- Essential for databases and stateful workloads.
- Core Kubernetes production topic.