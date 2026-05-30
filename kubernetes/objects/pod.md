# Pod

## Overview

Pod is the smallest deployable unit in Kubernetes.

A Pod represents one or more containers running together and sharing networking and storage resources.

Kubernetes schedules workloads at the Pod level.

---

## Responsibilities

Pod provides:

- Workload execution unit
- Shared network namespace
- Shared storage access
- Container grouping mechanism

---

## Pod Structure

Common Pod components:

- Application container
- Networking configuration
- Storage definitions
- Resource allocation settings

Pods are created and managed by Kubernetes controllers such as Deployments.

---

## Deployment Relationship

Example flow:

Container Image

↓

Pod

↓

Deployment

↓

Worker Node

Kubernetes manages workload lifecycle by scheduling Pods across available worker nodes.

---

## Design Consideration

A common deployment approach is to keep containers grouped by workload responsibility.

This helps improve operational management and workload organization.

---

## Notes

Pods are temporary by nature. Kubernetes controllers help maintain workload availability by recreating Pods when required.
# Pod

## Overview

A Pod is the smallest deployable unit in Kubernetes.

Pods are the basic execution unit used to run containerized workloads inside a Kubernetes cluster.

A Pod can contain:

- One Container
- Multiple Containers

Containers inside a Pod share:

- Network Namespace
- IP Address
- Port Space
- Volumes

---

## Why Pods Matter

Kubernetes does not schedule containers directly.

Instead:

```text
Container
     ↓
Pod
     ↓
Node
```

All workloads eventually run inside Pods.

---

## Pod Architecture

```text
Pod
├── Container A
├── Container B
└── Shared Storage
```

Containers inside the same Pod communicate using:

```text
localhost
```

---

## Responsibilities

### Workload Execution

Pods run application containers.

Examples:

- Web Applications
- APIs
- Batch Jobs
- Background Services

---

### Shared Networking

Every Pod receives its own IP address.

Example:

```text
Pod IP
10.244.1.10
```

Containers inside the Pod share this network.

---

### Shared Storage

Containers can share volumes.

Example:

```text
Container A
      ↓
 Shared Volume
      ↑
Container B
```

---

## Pod Lifecycle

Common States:

```text
Pending
   ↓
Running
   ↓
Succeeded
```

or

```text
Pending
   ↓
Running
   ↓
Failed
```

---

## Pod Characteristics

Important:

```text
Pods Are Ephemeral
```

Pods can be:

- Created
- Recreated
- Rescheduled
- Deleted

Pod IP addresses may change after recreation.

---

## Pod vs Container

| Pod | Container |
| ---- | --------- |
| Kubernetes Object | Runtime Process |
| Contains Containers | Runs Application |
| Scheduled By Kubernetes | Runs Inside Pod |
| Can Have Multiple Containers | Single Execution Unit |

---

## Pod vs Deployment

| Pod | Deployment |
| ---- | ---------- |
| Single Workload Instance | Manages Multiple Pods |
| No Self Healing | Supports Self Healing |
| No Scaling | Supports Scaling |
| Rarely Used Directly In Production | Common Production Pattern |

---

## Real Production Example

```text
Deployment
      ↓
3 Pods
      ↓
Containerized Application
```

If one Pod fails:

```text
Deployment
      ↓
Creates Replacement Pod
```

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- CrashLoopBackOff
- Image Pull Errors
- Pending Pods
- Resource Constraints
- Container Startup Failures

---

## Most Asked Interview Questions

1. What is a Pod?
2. Why is a Pod the smallest deployable unit?
3. Can a Pod contain multiple containers?
4. Do containers inside a Pod share networking?
5. What is a sidecar container?
6. Pod vs Container?
7. Pod vs Deployment?
8. Why are Pods considered ephemeral?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Pod is the smallest deployable unit.
- Kubernetes schedules Pods, not containers.
- Pods can contain one or more containers.
- Containers inside a Pod share networking and storage.
- Pods are ephemeral.
- Deployments manage Pods in production.