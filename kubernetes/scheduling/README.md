

# Scheduling

## Overview

Scheduling is the Kubernetes process of deciding where Pods should run inside a cluster.

The Kubernetes Scheduler evaluates cluster resources, constraints, policies, and workload requirements before assigning Pods to worker nodes.

---

## Why Scheduling Matters

Without scheduling decisions:

```text
Pod Created
     ↓
No Node Assignment
     ↓
Application Cannot Run
```

With scheduling:

```text
Pod Created
     ↓
Scheduler Evaluates Cluster
     ↓
Best Node Selected
     ↓
Pod Runs
```

Benefits:

- Efficient Resource Utilization
- High Availability
- Better Performance
- Workload Isolation
- Fault Tolerance

---

## Topics

### Scheduling Fundamentals

- Scheduler Overview
- Node Selector

### Advanced Scheduling

- Affinity And Anti-Affinity
- Taints And Tolerations

### Resource Management

- Resource Requests And Limits

---

## Scheduling Flow

```text
Pod Created
     ↓
Scheduler Detects Pending Pod
     ↓
Evaluate Nodes
     ↓
Apply Scheduling Rules
     ↓
Select Best Node
     ↓
Pod Scheduled
```

---

## Common Scheduling Controls

### Node Selector

Simple node placement using labels.

### Affinity

Attract Pods toward specific nodes or workloads.

### Anti-Affinity

Separate workloads for availability.

### Taints

Prevent Pods from running on specific nodes.

### Tolerations

Allow Pods to run on tainted nodes.

---

## Real Production Example

```text
GPU Workload
      ↓
Node Selector
      ↓
GPU Nodes

Database Cluster
      ↓
Pod Anti-Affinity
      ↓
Multiple Nodes
```

---

## Related Sections

- Architecture
- Worker Node
- Objects
- Operations
- Security

---

## Most Asked Interview Questions

1. What is the Kubernetes Scheduler?
2. How does Pod scheduling work?
3. What is Node Selector?
4. What is Affinity?
5. What are Taints and Tolerations?
6. Why do Pods remain Pending?
7. Affinity vs Taints?
8. How does Kubernetes choose a node?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Scheduler assigns Pods to nodes.
- Node Selector provides simple placement.
- Affinity influences placement.
- Taints repel Pods.
- Tolerations allow exceptions.
- Resource requests influence scheduling decisions.
- Scheduling is fundamental to Kubernetes operations.