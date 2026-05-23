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