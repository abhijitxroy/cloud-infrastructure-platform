

# Cluster Architecture

## Overview

A Kubernetes Cluster is a distributed system that manages containerized applications across multiple machines.

The cluster consists of two major parts:

- Control Plane
- Worker Nodes

Together they provide:

- Container Orchestration
- Scaling
- Self-Healing
- Service Discovery
- High Availability

---

## High Level Architecture

```text
Users / CI-CD
        ↓
     Kubectl
        ↓
    API Server
        ↓
 ┌───────────────┐
 │ Control Plane │
 └───────────────┘
        ↓
 ┌───────────────┐
 │ Worker Nodes  │
 └───────────────┘
        ↓
       Pods
        ↓
   Applications
```

---

## Control Plane

The Control Plane manages the cluster.

Core Components:

- API Server
- ETCD
- Scheduler
- Controller Manager

Responsibilities:

- Cluster State Management
- Scheduling Decisions
- Desired State Enforcement
- Configuration Storage

---

## Worker Nodes

Worker Nodes run application workloads.

Core Components:

- Kubelet
- Kube Proxy
- Container Runtime

Responsibilities:

- Running Pods
- Managing Containers
- Reporting Node Health
- Handling Network Communication

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

## Cluster Communication

Important Rule:

```text
All Components
      ↓
Communicate Through
      ↓
API Server
```

Benefits:

- Consistency
- Security
- Centralized Control

---

## Desired State Model

Kubernetes continuously compares:

```text
Desired State
      vs
Current State
```

Examples:

- Pod Recovery
- Replica Management
- Rolling Updates
- Auto Healing

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
- Reliability
- Reduced Downtime

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

- Control Plane Failure
- Node Failure
- Scheduling Problems
- ETCD Issues
- API Server Latency

---

## Most Asked Interview Questions

1. What is a Kubernetes Cluster?
2. What are the major cluster components?
3. Control Plane vs Worker Node?
4. What is the role of ETCD?
5. How does scheduling work?
6. How does Kubernetes achieve self-healing?
7. How is high availability implemented?
8. What happens when a node fails?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- A cluster consists of Control Plane and Worker Nodes.
- API Server is the entry point.
- ETCD stores cluster state.
- Scheduler places Pods.
- Worker Nodes run workloads.
- Kubernetes continuously maintains desired state.
- Fundamental Kubernetes architecture topic.