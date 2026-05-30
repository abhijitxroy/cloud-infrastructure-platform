# Control Plane

Cluster management components responsible for orchestration and scheduling.
# Control Plane

## Overview

The Control Plane is the management layer of Kubernetes.

It is responsible for:

- Cluster Management
- Scheduling Decisions
- Desired State Management
- API Processing
- Workload Orchestration

The Control Plane continuously ensures that the actual cluster state matches the desired state.

---

## Components

```text
Control Plane
├── API Server
├── Scheduler
├── Controller Manager
└── ETCD
```

---

## Responsibilities

- Accept Cluster Requests
- Store Cluster State
- Schedule Pods
- Manage Replicas
- Perform Self-Healing
- Coordinate Cluster Operations

---

## Request Flow

```text
Kubectl
    ↓
API Server
    ↓
ETCD
    ↓
Scheduler
    ↓
Controller Manager
    ↓
Worker Nodes
```

---

## Topics

- API Server
- Scheduler
- Controller Manager
- ETCD

---

## Most Asked Interview Questions

1. What is the Kubernetes Control Plane?
2. What are the major Control Plane components?
3. What happens if the API Server is unavailable?
4. Why is ETCD important?
5. How does scheduling work?
6. How does Kubernetes maintain desired state?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- The Control Plane manages the Kubernetes cluster.
- API Server is the entry point.
- ETCD stores cluster state.
- Scheduler places Pods.
- Controllers maintain desired state.
- Fundamental Kubernetes architecture topic.