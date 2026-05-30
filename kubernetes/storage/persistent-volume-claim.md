

# Persistent Volume Claim (PVC)

## Overview

A Persistent Volume Claim (PVC) is a Kubernetes object used by applications to request storage.

PVC acts as a storage request made by a Pod.

Instead of directly using storage infrastructure, applications request storage through PVCs.

---

## Why PVC Matters

Without PVC:

```text
Application
      ↓
Direct Storage Dependency
      ↓
Tight Coupling
```

With PVC:

```text
Application
      ↓
PVC
      ↓
Persistent Volume
      ↓
Storage System
```

Benefits:

- Storage Abstraction
- Portability
- Simplified Storage Management
- Better Flexibility

---

## PVC Architecture

```text
Pod
 ↓
PVC
 ↓
Persistent Volume
 ↓
Storage Backend
```

PVC requests storage while PV provides storage.

---

## How PVC Works

### Step 1

Application creates a PVC.

```text
Request 10Gi Storage
```

---

### Step 2

Kubernetes searches for a matching PV.

---

### Step 3

PVC binds to the PV.

```text
PVC ↔ PV
```

---

### Step 4

Pod mounts the PVC.

---

## PVC Components

### Storage Size

Example:

```text
10Gi
50Gi
100Gi
```

---

### Access Modes

#### ReadWriteOnce (RWO)

```text
Single Node Read/Write
```

---

#### ReadOnlyMany (ROX)

```text
Multiple Nodes Read Only
```

---

#### ReadWriteMany (RWX)

```text
Multiple Nodes Read/Write
```

---

## PVC vs PV

| PVC | PV |
| ---- | --- |
| Requests Storage | Provides Storage |
| Created By Application Team | Created Dynamically Or By Admin |
| Consumer | Provider |
| Pod Facing | Infrastructure Facing |

---

## Dynamic Provisioning

Modern Kubernetes clusters commonly use:

```text
PVC
 ↓
StorageClass
 ↓
Automatic PV Creation
```

Benefits:

- No Manual PV Creation
- Faster Provisioning
- Better Automation

---

## Real Production Example

```text
MySQL Pod
     ↓
PVC
     ↓
100Gi Storage
     ↓
Cloud Disk
```

If the Pod restarts:

```text
Data Remains Available
```

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- PVC Pending State
- PV Binding Failures
- StorageClass Misconfiguration
- Access Mode Mismatch
- Capacity Constraints

---

## Most Asked Interview Questions

1. What is a PVC?
2. Why is PVC needed?
3. PVC vs PV?
4. How does PVC binding work?
5. What are access modes?
6. What is dynamic provisioning?
7. Why is a PVC stuck in Pending state?
8. How do StatefulSets use PVCs?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- PVC is a request for storage.
- PV provides storage.
- Pods use PVCs, not PVs directly.
- PVCs abstract storage implementation details.
- Dynamic provisioning uses StorageClasses.
- Core Kubernetes storage topic.