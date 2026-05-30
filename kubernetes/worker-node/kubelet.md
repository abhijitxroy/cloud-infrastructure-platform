# Kubelet

## Overview

Kubelet is the primary node agent that runs on each worker node in a Kubernetes cluster.

It is responsible for ensuring workloads assigned to a node are running as expected.

Kubelet continuously communicates with the Kubernetes Control Plane and helps maintain workload health.

---

## Responsibilities

Common responsibilities:

- Register worker nodes with the cluster
- Monitor Pod health
- Start containers
- Stop containers
- Report node status
- Maintain workload state

---

## Pod Management

Kubelet works with Pod specifications provided through Kubernetes APIs.

A Pod specification defines workload configuration requirements such as:

- Container image
- Resource configuration
- Environment variables
- Storage definitions

Kubelet ensures workloads running on the node align with expected configuration.

---

## Cluster Communication

Example interaction flow:

Control Plane

↓

API Server

↓

Kubelet

↓

Container Runtime

↓

Application Workload

---

## Notes

Kubelet is one of the core worker node components responsible for maintaining workload execution and node level operational stability.
# Kubelet

## Overview

Kubelet is the primary node agent that runs on every Kubernetes worker node.

It is responsible for ensuring that Pods assigned to the node are running correctly and match the desired state defined in Kubernetes.

Kubelet continuously communicates with the Kubernetes API Server and manages workload execution on the node.

---

## Why Kubelet Matters

Without Kubelet:

```text
Pod Scheduled
      ↓
No Workload Execution
      ↓
Application Cannot Run
```

With Kubelet:

```text
Pod Scheduled
      ↓
Kubelet
      ↓
Container Runtime
      ↓
Application Running
```

Benefits:

- Workload Execution
- Node Management
- Health Monitoring
- Desired State Enforcement

---

## Architecture

```text
Control Plane
      ↓
API Server
      ↓
Kubelet
      ↓
Container Runtime
      ↓
Containers
```

Kubelet runs on every worker node.

---

## Core Responsibilities

### Node Registration

Registers the worker node with the Kubernetes cluster.

---

### Pod Lifecycle Management

Responsible for:

- Creating Pods
- Starting Containers
- Stopping Containers
- Removing Containers

---

### Health Monitoring

Continuously monitors:

- Pods
- Containers
- Node Health

---

### Status Reporting

Reports information back to the API Server.

Examples:

- Node Status
- Pod Status
- Resource Usage Information

---

## Kubelet Workflow

```text
Pod Scheduled
      ↓
Kubelet Receives Pod Spec
      ↓
Container Runtime Pulls Image
      ↓
Containers Started
      ↓
Health Monitoring
```

---

## Pod Specification Management

Kubelet works with Pod specifications.

Examples:

- Container Images
- Resource Requests
- Resource Limits
- Environment Variables
- Volumes
- Networking Configuration

Kubelet ensures workloads match the declared configuration.

---

## Kubelet and Container Runtime

Kubelet does not run containers directly.

It communicates through:

```text
CRI
(Container Runtime Interface)
```

Examples:

- containerd
- CRI-O

---

## Kubelet vs Kube Proxy

| Kubelet | Kube Proxy |
| -------- | ---------- |
| Manages Workloads | Manages Networking |
| Runs Pods | Routes Traffic |
| Node Agent | Network Component |
| Container Lifecycle | Service Connectivity |

---

## Real Production Example

```text
Deployment Created
         ↓
Scheduler Selects Node
         ↓
Kubelet Receives Assignment
         ↓
Container Runtime Starts Containers
         ↓
Application Available
```

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Node Not Ready
- Pod Startup Failures
- Runtime Communication Issues
- Resource Exhaustion
- Health Reporting Problems

---

## Most Asked Interview Questions

1. What is Kubelet?
2. Why is Kubelet needed?
3. What are Kubelet responsibilities?
4. How does Kubelet communicate with the API Server?
5. Kubelet vs Kube Proxy?
6. How does Kubelet work with container runtimes?
7. What happens when a Pod is scheduled?
8. Why is Kubelet considered a node agent?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Kubelet runs on every worker node.
- Kubelet manages Pod execution.
- Kubelet communicates with the API Server.
- Kubelet uses CRI to interact with runtimes.
- Kubelet enforces desired state.
- One of the most important Kubernetes architecture topics.