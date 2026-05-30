

# Persistent Volume (PV)

## Overview

A Persistent Volume (PV) is a Kubernetes storage resource that provides persistent storage for applications.

Unlike container storage, Persistent Volumes exist independently of Pods and survive Pod restarts, rescheduling, and recreation.

PV abstracts the underlying storage infrastructure from applications.

---

## Why Persistent Volumes Matter

Without Persistent Volumes:

```text
Pod Deleted
     ↓
Data Lost
```

With Persistent Volumes:

```text
Pod Deleted
     ↓
Data Preserved
     ↓
New Pod Uses Same Data
```

Benefits:

- Persistent Data
- Storage Independence
- Better Reliability
- Stateful Workload Support

---

## PV Architecture

```text
Pod
 ↓
PVC
 ↓
PV
 ↓
Storage Backend
```

Examples of storage backends:

- AWS EBS
- Azure Disk
- Google Persistent Disk
- NFS
- Ceph
- SAN Storage

---

## How Persistent Volumes Work

### Step 1

Storage is provisioned.

---

### Step 2

Persistent Volume is created.

---

### Step 3

Persistent Volume Claim requests storage.

---

### Step 4

PVC binds to the PV.

---

### Step 5

Pod mounts the storage.

---

## PV Lifecycle

```text
Available
    ↓
Bound
    ↓
Released
    ↓
Reclaimed
```

### Available

Storage is ready to be used.

### Bound

PV is attached to a PVC.

### Released

PVC has been deleted.

### Reclaimed

Storage cleanup process occurs.

---

## Access Modes

### ReadWriteOnce (RWO)

```text
Single Node Read/Write
```

---

### ReadOnlyMany (ROX)

```text
Multiple Nodes Read Only
```

---

### ReadWriteMany (RWX)

```text
Multiple Nodes Read/Write
```

---

## Reclaim Policies

### Retain

```text
Keep Storage After PVC Deletion
```

Used when data must be preserved.

---

### Delete

```text
Delete Storage Automatically
```

Common in cloud environments.

---

### Recycle (Legacy)

Rarely used in modern Kubernetes environments.

---

## PV vs PVC

| PV | PVC |
| --- | --- |
| Provides Storage | Requests Storage |
| Infrastructure Resource | Application Resource |
| Storage Provider | Storage Consumer |
| Backend Focused | Workload Focused |

---

## Real Production Example

```text
PostgreSQL Database
         ↓
PVC
         ↓
Persistent Volume
         ↓
Cloud Block Storage
```

If the database Pod restarts:

```text
Data Remains Available
```

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- PV Not Bound
- Storage Capacity Issues
- Access Mode Mismatch
- Reclaim Policy Problems
- Storage Backend Failures

---

## Most Asked Interview Questions

1. What is a Persistent Volume?
2. Why are Persistent Volumes needed?
3. PV vs PVC?
4. What are access modes?
5. What are reclaim policies?
6. How does PV binding work?
7. What happens when a Pod is deleted?
8. Why are PVs important for databases?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- PV provides persistent storage.
- PV exists independently of Pods.
- PVC requests storage from PV.
- Access modes control storage usage.
- Reclaim policies control storage cleanup.
- Essential Kubernetes storage topic.