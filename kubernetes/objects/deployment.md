# Deployment

## Overview

Deployment is a Kubernetes resource used to manage application workloads running inside Pods.

Deployments help maintain application availability and simplify workload updates over time.

Kubernetes uses Deployments to manage Pod lifecycle operations automatically.

---

## Responsibilities

Common responsibilities:

- Pod creation
- Scaling workloads
- Rolling updates
- Workload recovery
- Replica management

---

## Replica Management

Deployments work with ReplicaSets to maintain the expected number of running Pods.

Example:

Desired replicas:

- 5

Current running replicas:

- 3

Kubernetes automatically attempts to restore the expected application state.

---

## Application Update Flow

Example workflow:

Application Update

↓

Deployment

↓

ReplicaSet

↓

Pod

↓

Worker Node

Deployments support workload changes while helping reduce service interruption.

---

## Scaling

Deployments allow workloads to scale based on application requirements.

Examples:

- Increase application instances
- Reduce workload instances
- Handle changing traffic patterns

---

## Notes

Deployment is one of the primary Kubernetes objects used for managing stateless application workloads and maintaining operational consistency.
# Deployment

## Overview

A Deployment is a Kubernetes workload object used to manage stateless applications.

Deployments provide declarative application management and automatically maintain the desired number of running Pods.

They are one of the most commonly used Kubernetes resources in production environments.

---

## Why Deployments Matter

Without Deployments:

```text
Pod Fails
    ↓
Application Unavailable
```

With Deployments:

```text
Pod Fails
    ↓
Deployment Detects Failure
    ↓
Replacement Pod Created
```

Benefits:

- Self Healing
- Scaling
- Rolling Updates
- Rollbacks
- High Availability

---

## Architecture

```text
Deployment
      ↓
ReplicaSet
      ↓
Pods
      ↓
Application
```

Deployments manage ReplicaSets.

ReplicaSets manage Pods.

---

## Responsibilities

### Pod Management

Creates and manages Pods automatically.

---

### Replica Management

Maintains the desired number of running Pods.

---

### Rolling Updates

Updates applications without significant downtime.

---

### Rollbacks

Allows reverting to a previous application version.

---

### Self Healing

Automatically recreates failed Pods.

---

## Replica Management Example

```text
Desired Replicas = 5
Running Replicas = 3
        ↓
Create 2 New Pods
```

Result:

```text
Running Replicas = 5
```

---

## Rolling Update Flow

```text
Version 1 Pods
        ↓
Deployment Update
        ↓
Version 2 Pods Created
        ↓
Version 1 Pods Removed
```

Benefits:

- Reduced Downtime
- Safer Releases
- Controlled Rollouts

---

## Rollback Example

```text
Version 2 Deployment
          ↓
Production Issue
          ↓
Rollback
          ↓
Version 1 Deployment
```

---

## Scaling Example

```text
Traffic Increase
       ↓
Replicas: 3 → 10
       ↓
Additional Pods Created
```

Benefits:

- Better Performance
- Improved Availability
- Increased Capacity

---

## Deployment vs Pod

| Deployment | Pod |
| ---------- | --- |
| Manages Pods | Runs Containers |
| Supports Scaling | Single Workload Instance |
| Supports Rolling Updates | No Update Management |
| Supports Rollbacks | No Rollback Capability |
| Production Ready | Building Block |

---

## Real Production Example

```text
E-Commerce Application
         ↓
Deployment
         ↓
10 Replicas
         ↓
Traffic Distributed Across Pods
```

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Pods Not Starting
- Failed Rollouts
- Replica Mismatch
- Image Pull Failures
- Scaling Issues

---

## Most Asked Interview Questions

1. What is a Deployment?
2. Why use Deployments instead of Pods?
3. How do Deployments perform rolling updates?
4. What is a ReplicaSet?
5. How do rollbacks work?
6. How does Kubernetes achieve self-healing?
7. How do Deployments scale workloads?
8. Deployment vs StatefulSet?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Deployments manage stateless workloads.
- Deployments create and manage ReplicaSets.
- ReplicaSets maintain Pod count.
- Deployments support rolling updates and rollbacks.
- Deployments enable self-healing and scaling.
- One of the most important Kubernetes interview topics.