

# Worker Node

## Overview

A Worker Node is a machine responsible for running application workloads inside a Kubernetes cluster.

Worker nodes execute Pods and provide the compute resources required by applications.

Every Kubernetes cluster contains one or more worker nodes.

---

## Why Worker Nodes Matter

Without Worker Nodes:

```text
Control Plane
      ↓
No Workload Execution
      ↓
Applications Cannot Run
```

With Worker Nodes:

```text
Control Plane
      ↓
Worker Nodes
      ↓
Pods Running
      ↓
Applications Available
```

Benefits:

- Workload Execution
- Application Hosting
- Resource Management
- Scalability

---

## Worker Node Architecture

```text
Worker Node
    ├── Kubelet
    ├── Kube Proxy
    └── Container Runtime
```

---

## Core Components

### Kubelet

Node agent responsible for:

- Pod Execution
- Health Monitoring
- Status Reporting

---

### Kube Proxy

Responsible for:

- Service Networking
- Traffic Routing
- Load Distribution

---

### Container Runtime

Responsible for:

- Image Management
- Container Execution
- Container Lifecycle

Examples:

- containerd
- CRI-O

---

## Workload Execution Flow

```text
Deployment
      ↓
Scheduler
      ↓
Worker Node
      ↓
Kubelet
      ↓
Container Runtime
      ↓
Container Running
```

---

## Responsibilities

### Run Pods

Worker nodes execute application workloads.

### Resource Management

Provides:

- CPU
- Memory
- Storage
- Network Resources

### Health Reporting

Continuously reports status to the control plane.

---

## Real Production Example

```text
E-Commerce Application
          ↓
Deployment
          ↓
10 Pods
          ↓
Worker Nodes
          ↓
Customer Traffic Served
```

---

## Related Sections

- Control Plane
- Scheduling
- Networking
- Storage

---

## Most Asked Interview Questions

1. What is a Worker Node?
2. What components run on a Worker Node?
3. What is Kubelet?
4. What is Kube Proxy?
5. What is a Container Runtime?
6. How do Worker Nodes execute Pods?
7. Worker Node vs Control Plane?
8. What happens when a Worker Node fails?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Worker Nodes run application workloads.
- Kubelet manages Pod execution.
- Kube Proxy manages networking.
- Container Runtime executes containers.
- Worker Nodes provide compute resources.
- Fundamental Kubernetes architecture topic.