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