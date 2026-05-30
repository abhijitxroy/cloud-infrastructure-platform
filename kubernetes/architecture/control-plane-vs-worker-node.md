

# Control Plane vs Worker Node

## Overview

A Kubernetes cluster is divided into two major parts:

- Control Plane
- Worker Nodes

Both are essential but serve different responsibilities.

```text
Control Plane
      ↓
Manages Cluster

Worker Nodes
      ↓
Run Applications
```

---

## Control Plane

The Control Plane is responsible for managing the cluster.

Core Components:

- API Server
- ETCD
- Scheduler
- Controller Manager

Responsibilities:

- Cluster Management
- Scheduling Decisions
- Desired State Management
- Configuration Storage
- Self-Healing Operations

---

## Worker Node

Worker Nodes execute application workloads.

Core Components:

- Kubelet
- Kube Proxy
- Container Runtime

Responsibilities:

- Running Pods
- Container Lifecycle Management
- Network Communication
- Resource Consumption

---

## Architecture View

```text
             Control Plane

 ┌─────────────────────────────┐
 │ API Server                  │
 │ ETCD                        │
 │ Scheduler                   │
 │ Controller Manager          │
 └─────────────────────────────┘
               ↓
 ┌─────────────────────────────┐
 │ Worker Node 1               │
 │  └── Pods                   │
 └─────────────────────────────┘

 ┌─────────────────────────────┐
 │ Worker Node 2               │
 │  └── Pods                   │
 └─────────────────────────────┘
```

---

## Responsibilities Comparison

| Control Plane | Worker Node |
|--------------|-------------|
| Manages Cluster | Runs Applications |
| Stores Cluster State | Executes Pods |
| Schedules Workloads | Consumes Resources |
| Maintains Desired State | Hosts Containers |
| Controls Operations | Runs Business Workloads |

---

## Failure Impact

### Control Plane Failure

Possible Impact:

```text
Management Operations Fail
Scheduling Stops
Cluster Changes Blocked
```

Existing Pods may continue running.

---

### Worker Node Failure

Possible Impact:

```text
Pods Become Unavailable
      ↓
Controllers Detect Failure
      ↓
Pods Recreated Elsewhere
```

Kubernetes self-healing helps recover workloads.

---

## Resource Usage

### Control Plane

Consumes resources for:

- Scheduling
- State Management
- Cluster Coordination

### Worker Nodes

Consume resources for:

- Applications
- Databases
- Services
- Containers

---

## Real Production Example

```text
3 Control Plane Nodes
        ↓
20 Worker Nodes
        ↓
500+ Pods
        ↓
Business Applications
```

---

## Production Engineering Perspective

### Common Troubleshooting Areas

Control Plane:

- API Server Issues
- ETCD Failures
- Scheduling Problems

Worker Nodes:

- Node Not Ready
- Pod Failures
- Resource Exhaustion

---

## Most Asked Interview Questions

1. What is the Control Plane?
2. What is a Worker Node?
3. Control Plane vs Worker Node?
4. What components exist in the Control Plane?
5. What components exist on Worker Nodes?
6. What happens if a Worker Node fails?
7. What happens if the Control Plane fails?
8. Which component runs application workloads?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Control Plane manages the cluster.
- Worker Nodes run workloads.
- API Server, ETCD, Scheduler and Controller Manager belong to the Control Plane.
- Kubelet, Kube Proxy and Container Runtime belong to Worker Nodes.
- Worker Node failures are handled through self-healing.
- Fundamental Kubernetes architecture interview topic.