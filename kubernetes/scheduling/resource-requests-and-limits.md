

# Resource Requests and Limits

## Overview

Resource Requests and Limits define how much CPU and memory a container requires and how much it is allowed to consume.

They help Kubernetes make scheduling decisions and prevent workloads from consuming excessive cluster resources.

---

## Why Requests and Limits Matter

Without Resource Controls:

```text
Application Uses Excessive Resources
                ↓
Other Workloads Impacted
                ↓
Cluster Instability
```

With Resource Controls:

```text
Defined Resources
        ↓
Controlled Consumption
        ↓
Stable Cluster
```

Benefits:

- Predictable Performance
- Better Scheduling
- Resource Isolation
- Improved Cluster Stability

---

## Resource Requests

A Request is the minimum resource amount required by a container.

The Scheduler uses requests when selecting a node.

Example:

```text
CPU Request    : 500m
Memory Request : 512Mi
```

Meaning:

```text
Scheduler Must Find
A Node With Available Capacity
```

---

## Resource Limits

A Limit is the maximum resource amount a container can consume.

Example:

```text
CPU Limit    : 1000m
Memory Limit : 1Gi
```

Meaning:

```text
Container Cannot Exceed
Configured Maximum Resources
```

---

## Requests vs Limits

| Requests | Limits |
| -------- | ------ |
| Minimum Required Resources | Maximum Allowed Resources |
| Used For Scheduling | Used For Enforcement |
| Guarantees Availability | Prevents Resource Abuse |
| Scheduler Focused | Runtime Focused |

---

## CPU Behavior

When CPU usage exceeds limits:

```text
CPU Throttling
```

The container continues running but performance may decrease.

---

## Memory Behavior

When memory usage exceeds limits:

```text
OOMKilled
```

The container may be terminated and restarted.

---

## Scheduling Flow

```text
Pod Created
      ↓
Resource Requests Evaluated
      ↓
Scheduler Selects Node
      ↓
Pod Scheduled
```

---

## Common Resource Units

### CPU

```text
1000m = 1 CPU Core
500m  = 0.5 CPU
250m  = 0.25 CPU
```

---

### Memory

```text
256Mi
512Mi
1Gi
2Gi
```

---

## Real Production Example

```text
Java Application
        ↓
Request
CPU    : 500m
Memory : 1Gi

Limit
CPU    : 2000m
Memory : 4Gi
```

Benefits:

- Reliable Scheduling
- Controlled Resource Consumption
- Improved Stability

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- OOMKilled Containers
- CPU Throttling
- Pods Stuck Pending
- Incorrect Resource Sizing
- Cluster Capacity Issues

---

## Most Asked Interview Questions

1. What are Resource Requests?
2. What are Resource Limits?
3. Requests vs Limits?
4. How does the Scheduler use Requests?
5. What is CPU throttling?
6. What is OOMKilled?
7. Why do Pods remain Pending?
8. How should resources be sized in production?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Requests are used for scheduling.
- Limits are used for enforcement.
- CPU limit violations cause throttling.
- Memory limit violations may cause OOMKilled.
- Proper sizing improves cluster stability.
- Frequently asked Kubernetes scheduling and operations topic.