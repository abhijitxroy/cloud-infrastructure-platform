# Controller Manager

## Overview

The Controller Manager is part of the Kubernetes Control Plane and is responsible for maintaining the desired state of the cluster.

Kubernetes continuously compares the current cluster state with the expected state and performs corrective actions when differences are detected.

---

## Responsibilities

Common responsibilities:

- Monitor cluster state
- Maintain workload availability
- Handle node related events
- Manage controller operations
- Recover workloads when failures occur

---

## Desired State vs Current State

Kubernetes follows a reconciliation model.

Example:

Desired state:

- Application replicas = 5

Current state:

- Running replicas = 3

Controller Manager detects the difference and works with other cluster components to restore the expected state.

---

## Operational Examples

Examples of controller driven operations:

- Restart failed workloads
- Replace unavailable Pods
- Maintain replica count
- Respond to node failures

---

## Notes

Controller based reconciliation is one of the core operational patterns that allows Kubernetes to maintain workload reliability and cluster stability.