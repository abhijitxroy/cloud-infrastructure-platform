

# Taints and Tolerations

## Overview

Taints and Tolerations are Kubernetes scheduling mechanisms used to control which Pods can run on specific nodes.

Taints are applied to nodes.

Tolerations are applied to Pods.

Together they help enforce workload isolation and scheduling policies.

---

## Why Taints and Tolerations Matter

Without Taints:

```text
Any Pod
    ↓
Any Suitable Node
```

With Taints:

```text
Node Protected
      ↓
Only Allowed Pods Scheduled
```

Benefits:

- Workload Isolation
- Dedicated Infrastructure
- Better Resource Management
- Improved Security

---

## Core Concept

### Taint

A Taint repels Pods from a node.

```text
Node
 ↓
Taint Applied
 ↓
Pods Rejected
```

---

### Toleration

A Toleration allows a Pod to run on a tainted node.

```text
Pod
 ↓
Toleration Added
 ↓
Node Access Allowed
```

---

## Scheduling Flow

```text
Pod Created
     ↓
Scheduler Evaluates Node
     ↓
Taint Found
     ↓
Toleration Exists?
     ↓
Yes → Schedule Pod
No  → Reject Pod
```

---

## Taint Effects

### NoSchedule

Prevents new Pods from being scheduled.

```text
Node
 ↓
NoSchedule
 ↓
New Pods Blocked
```

---

### PreferNoSchedule

Soft scheduling restriction.

Scheduler tries to avoid the node.

```text
Best Effort Restriction
```

---

### NoExecute

Removes existing Pods that do not tolerate the taint.

```text
Taint Added
      ↓
Non-Tolerating Pods Evicted
```

---

## Common Use Cases

### Dedicated Nodes

```text
Production Nodes
       ↓
Only Production Workloads
```

---

### GPU Nodes

```text
GPU Nodes
     ↓
Only ML Workloads
```

---

### System Workloads

```text
Infrastructure Nodes
        ↓
Monitoring
Logging
Security Agents
```

---

### Maintenance Activities

```text
Node Maintenance
        ↓
NoExecute Taint
        ↓
Workloads Moved
```

---

## Taints vs Affinity

| Taints | Affinity |
| -------- | -------- |
| Repels Pods | Attracts Pods |
| Applied To Nodes | Applied To Pods |
| Restrictive | Placement Preference |
| Isolation Focused | Placement Focused |

---

## Real Production Example

```text
GPU Node
    ↓
gpu=true
    ↓
Taint Applied
    ↓
Only ML Pods With Toleration
```

Benefits:

- Dedicated Hardware Usage
- Better Resource Isolation

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Pods Stuck Pending
- Missing Tolerations
- Incorrect Taint Effects
- Node Isolation Problems
- Unexpected Pod Evictions

---

## Most Asked Interview Questions

1. What are Taints and Tolerations?
2. Why are Taints used?
3. What is a Toleration?
4. NoSchedule vs PreferNoSchedule?
5. What is NoExecute?
6. Taints vs Affinity?
7. Why is a Pod stuck Pending?
8. How are dedicated nodes implemented?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Taints repel Pods.
- Tolerations allow exceptions.
- Taints are applied to nodes.
- Tolerations are applied to Pods.
- NoSchedule blocks scheduling.
- NoExecute can evict running Pods.
- Frequently asked Kubernetes scheduling topic.