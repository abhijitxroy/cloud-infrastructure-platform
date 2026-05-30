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
# Self Healing

## Overview

Self Healing is the Kubernetes capability that automatically detects failures and restores workloads to their desired state.

Kubernetes continuously compares:

```text
Desired State
      vs
Current State
```

When a mismatch is detected, Kubernetes automatically takes corrective actions.

---

## Why Self Healing Matters

Without Self Healing:

```text
Pod Failure
     ↓
Application Outage
     ↓
Manual Recovery
```

With Self Healing:

```text
Pod Failure
     ↓
Kubernetes Detects Issue
     ↓
Replacement Pod Created
```

Benefits:

- Higher Availability
- Faster Recovery
- Reduced Downtime
- Improved Reliability

---

## How Self Healing Works

```text
Failure Occurs
      ↓
Controller Detects Failure
      ↓
Desired State Violated
      ↓
Recovery Action Triggered
      ↓
Desired State Restored
```

---

## Common Recovery Scenarios

### Pod Failure

```text
Pod Crashes
      ↓
ReplicaSet Detects Failure
      ↓
New Pod Created
```

---

### Container Failure

```text
Container Stops
       ↓
Kubelet Detects Failure
       ↓
Container Restarted
```

---

### Node Failure

```text
Worker Node Fails
        ↓
Pods Become Unavailable
        ↓
Pods Rescheduled
        ↓
Application Restored
```

---

### Probe Failure

```text
Liveness Probe Fails
         ↓
Container Restarted
```

---

## Kubernetes Components Involved

### Deployment

Maintains desired replica count.

### ReplicaSet

Creates replacement Pods.

### Controller Manager

Monitors cluster state.

### Kubelet

Restarts failed containers.

---

## Real Production Example

```text
Deployment
    ↓
5 Replicas
    ↓
1 Pod Crashes
    ↓
ReplicaSet Detects Failure
    ↓
Replacement Pod Created
    ↓
5 Replicas Restored
```

---

## Self Healing vs Monitoring

| Self Healing | Monitoring |
| ------------ | ---------- |
| Automatic Recovery | Detects Problems |
| Corrective Action | Visibility |
| Restores State | Reports State |
| Reduces Downtime | Improves Awareness |

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Pods Not Recreated
- Failed Health Probes
- Resource Exhaustion
- Node Failures
- Scheduling Constraints

---

## Most Asked Interview Questions

1. What is Kubernetes Self Healing?
2. How does Kubernetes detect failures?
3. What happens when a Pod crashes?
4. What happens when a node fails?
5. How do ReplicaSets support self-healing?
6. What role do probes play?
7. How does Kubernetes maintain desired state?
8. Self Healing vs High Availability?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Self Healing restores workloads automatically.
- Kubernetes continuously maintains desired state.
- ReplicaSets recreate failed Pods.
- Kubelet restarts failed containers.
- Probes help detect unhealthy applications.
- One of Kubernetes' most important production capabilities.