

# StorageClass

## Overview

A StorageClass is a Kubernetes object that defines how Persistent Volumes are dynamically provisioned.

StorageClasses eliminate the need to manually create Persistent Volumes before applications request storage.

They act as templates that describe storage characteristics and provisioning behavior.

---

## Why StorageClass Matters

Without StorageClass:

```text
Administrator
      ↓
Manually Create PV
      ↓
Application Uses PVC
```

With StorageClass:

```text
Application Creates PVC
          ↓
StorageClass
          ↓
Automatic PV Creation
```

Benefits:

- Dynamic Provisioning
- Faster Deployments
- Reduced Administrative Work
- Better Scalability

---

## Storage Architecture

```text
Pod
 ↓
PVC
 ↓
StorageClass
 ↓
PV
 ↓
Storage Backend
```

---

## How StorageClass Works

### Step 1

Application creates a PVC.

---

### Step 2

PVC references a StorageClass.

---

### Step 3

StorageClass provisions storage automatically.

---

### Step 4

A Persistent Volume is created.

---

### Step 5

PVC binds to the newly created PV.

---

## Common Storage Backends

Examples:

- AWS EBS
- Azure Disk
- Google Persistent Disk
- NFS
- Ceph
- NetApp

---

## StorageClass Components

### Provisioner

Defines which storage provider creates volumes.

Example:

```text
AWS EBS Provisioner
```

---

### Reclaim Policy

Defines what happens after PVC deletion.

Options:

```text
Delete
Retain
```

---

### Volume Binding Mode

Controls when storage is provisioned.

Common Modes:

```text
Immediate
WaitForFirstConsumer
```

---

## Static vs Dynamic Provisioning

| Static Provisioning | Dynamic Provisioning |
| ------------------- | -------------------- |
| Manual PV Creation | Automatic PV Creation |
| More Administration | Less Administration |
| Slower Provisioning | Faster Provisioning |
| Traditional Approach | Modern Approach |

---

## StorageClass vs PV vs PVC

| Component | Responsibility |
| ---------- | ------------- |
| StorageClass | Defines Provisioning Rules |
| PV | Provides Storage |
| PVC | Requests Storage |

---

## Real Production Example

```text
PostgreSQL Application
         ↓
PVC
         ↓
gp3 StorageClass
         ↓
AWS EBS Volume
         ↓
PV Created Automatically
```

Benefits:

- Automated Provisioning
- Faster Deployments
- Reduced Operational Effort

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Missing StorageClass
- Provisioning Failures
- Incorrect Provisioner
- PVC Pending State
- Storage Quota Issues

---

## Most Asked Interview Questions

1. What is a StorageClass?
2. Why is StorageClass needed?
3. Static vs Dynamic Provisioning?
4. How does StorageClass work with PVCs?
5. What is a provisioner?
6. What is WaitForFirstConsumer?
7. StorageClass vs PV vs PVC?
8. Why is a PVC stuck in Pending state?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- StorageClass enables dynamic provisioning.
- PVC requests storage.
- StorageClass creates PV automatically.
- Modern Kubernetes clusters use dynamic provisioning.
- Reduces manual storage administration.
- Essential Kubernetes storage topic.