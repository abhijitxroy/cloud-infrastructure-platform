# Architecture

## Overview

Kubernetes architecture follows a distributed control model consisting of cluster management components and workload execution components.

A Kubernetes cluster is organized into:

- Control Plane
- Worker Nodes

The Control Plane manages cluster state and operational decisions.

Worker Nodes execute application workloads.

---

## Why Architecture Matters

Understanding Kubernetes architecture helps engineers:

- Troubleshoot Production Issues
- Understand Scheduling Decisions
- Debug Cluster Failures
- Design Highly Available Clusters
- Operate Kubernetes At Scale

---

## High Level Architecture

```text
Users / CI-CD
       ↓
    Kubectl
       ↓
   API Server
       ↓
┌──────────────┐
│ Control Plane│
└──────────────┘
       ↓
┌──────────────┐
│ Worker Nodes │
└──────────────┘
       ↓
      Pods
       ↓
 Applications
```

---

## Control Plane Components

Core Components:

- API Server
- Scheduler
- Controller Manager
- ETCD

Responsibilities:

- Cluster State Management
- Scheduling Decisions
- Desired State Enforcement
- Configuration Storage

---

## Worker Node Components

Core Components:

- Kubelet
- Kube Proxy
- Container Runtime

Responsibilities:

- Pod Execution
- Container Lifecycle Management
- Node Health Reporting
- Service Networking

---

## Request Flow

```text
Kubectl
    ↓
API Server
    ↓
ETCD Updated
    ↓
Scheduler Selects Node
    ↓
Kubelet Creates Pod
    ↓
Application Running
```

---

## Control Plane Responsibilities

Examples:

- Cluster State Management
- API Processing
- Workload Scheduling
- Replica Management
- Rolling Updates

---

## Worker Node Responsibilities

Examples:

- Running Containers
- Monitoring Pods
- Reporting Node Status
- Managing Local Resources

---

## Operational Model

Kubernetes continuously compares:

```text
Desired State
      vs
Current State
```

Examples:

- Workload Recovery
- Scaling Operations
- Deployment Updates
- Self Healing

---

## High Availability Architecture

Production clusters typically use:

```text
Load Balancer
       ↓
Multiple Control Plane Nodes
       ↓
Multiple Worker Nodes
```

Benefits:

- Fault Tolerance
- Better Reliability
- Reduced Downtime

---

## Production Example

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

## Related Topics

- Cluster Architecture
- Control Plane vs Worker Node
- API Server
- Scheduler
- Controller Manager
- ETCD
- Kubelet
- Kube Proxy

---

## Most Asked Interview Questions

1. What is Kubernetes Architecture?
2. What are the major Kubernetes components?
3. What is the Control Plane?
4. What is a Worker Node?
5. What is the role of the API Server?
6. Why is ETCD important?
7. How does scheduling work?
8. How does Kubernetes achieve self-healing?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Kubernetes consists of Control Plane and Worker Nodes.
- API Server is the cluster entry point.
- ETCD stores cluster state.
- Scheduler places Pods on nodes.
- Controllers maintain desired state.
- Worker Nodes run application workloads.
- Architecture is a foundational Kubernetes interview topic.