# Self Healing

## Overview

Self healing is the ability of Kubernetes to automatically recover workloads when failures occur.

Kubernetes continuously monitors workload state and attempts to maintain application availability based on expected configuration.

This reduces manual operational effort and improves platform reliability.

---

## Recovery Scenarios

Examples:

### Pod Failure

If a Pod becomes unavailable, Kubernetes controllers attempt to create replacement workloads.

### Node Failure

If a worker node becomes unavailable, Kubernetes can reschedule workloads to healthy nodes when cluster capacity is available.

### Container Failure

Containers that stop unexpectedly can be restarted automatically.

---

## Operational Benefits

Self healing helps improve:

- Application availability
- Platform resilience
- Failure recovery capability
- Operational stability

---

## Kubernetes Components Involved

Examples:

- Deployment
- ReplicaSet
- Controller Manager
- Kubelet

These components work together to maintain expected workload state.

---

## Notes

Self healing is one of the operational capabilities that helps Kubernetes support large scale containerized environments with reduced manual intervention.