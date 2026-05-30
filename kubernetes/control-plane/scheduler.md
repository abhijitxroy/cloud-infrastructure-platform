# Scheduler

## Overview

The Kubernetes Scheduler is responsible for selecting an appropriate worker node for workloads that need placement inside the cluster.

When a Pod is created without an assigned node, the Scheduler evaluates available worker nodes and determines a suitable location.

---

## Responsibilities

Common responsibilities:

- Select worker nodes
- Evaluate resource availability
- Support workload distribution
- Improve cluster resource utilization

---

## Scheduling Process

Scheduling generally involves two stages.

### Filtering

Worker nodes are evaluated to identify nodes capable of running the workload.

Examples:

- Resource availability
- Node constraints
- Scheduling requirements

### Scoring

Remaining candidate nodes are ranked based on scheduling rules.

The Scheduler selects an appropriate worker node based on evaluation results.

---

## Examples

Scheduling decisions may consider:

- CPU availability
- Memory capacity
- Node affinity rules
- Taints and tolerations
- Resource allocation requirements

---

## Notes

Scheduling decisions influence workload placement efficiency and overall cluster resource utilization.
# Scheduler

## Overview

The Kubernetes Scheduler is a Control Plane component responsible for selecting the most appropriate worker node for a Pod.

When a Pod is created without a node assignment, the Scheduler evaluates available worker nodes and determines where the Pod should run.

The Scheduler does not run containers.

Its responsibility is:

```text
Pod Created
      ↓
Select Best Node
      ↓
Assign Pod
```

---

## Why Scheduler Matters

Without the Scheduler:

```text
Pod Created
      ↓
No Node Selected
      ↓
Application Cannot Run
```

The Scheduler enables:

- Workload Placement
- Resource Optimization
- Cluster Efficiency
- High Availability
- Scalability

---

## Architecture Position

```text
Kubectl
    ↓
API Server
    ↓
ETCD
    ↓
Scheduler
    ↓
Worker Node Selected
    ↓
Kubelet Starts Pod
```

---

## Responsibilities

### Node Selection

Selects the most suitable node for a Pod.

---

### Resource Evaluation

Checks:

- CPU Availability
- Memory Availability
- Resource Requests
- Resource Limits

---

### Constraint Evaluation

Considers:

- Node Selectors
- Affinity Rules
- Anti-Affinity Rules
- Taints
- Tolerations

---

### Workload Distribution

Attempts to distribute workloads efficiently across nodes.

Benefits:

- Better Utilization
- Improved Reliability
- Reduced Hotspots

---

## Scheduling Process

### Step 1: Filtering

Identify nodes capable of running the workload.

Examples:

- Available CPU
- Available Memory
- Scheduling Constraints

Result:

```text
Eligible Nodes
```

---

### Step 2: Scoring

Rank eligible nodes.

Factors:

- Resource Utilization
- Scheduling Preferences
- Placement Rules

Result:

```text
Best Node Selected
```

---

## Scheduling Factors

Examples:

- CPU Availability
- Memory Capacity
- Node Affinity
- Pod Affinity
- Taints And Tolerations
- Resource Requests
- Resource Limits

---

## Real Production Example

```text
Deployment Created
        ↓
10 Pods Requested
        ↓
Scheduler Evaluates Nodes
        ↓
Pods Distributed Across Cluster
        ↓
Application Becomes Available
```

---

## Common Scheduling Features

### Node Selector

Schedule workloads to specific nodes.

### Affinity

Prefer specific node placement.

### Anti-Affinity

Avoid specific node placement.

### Taints And Tolerations

Control workload placement rules.

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Pending Pods
- Insufficient Resources
- Affinity Misconfiguration
- Taint Conflicts
- Uneven Workload Distribution

---

## Most Asked Interview Questions

1. What is the Kubernetes Scheduler?
2. What is the role of the Scheduler?
3. How does scheduling work?
4. What is filtering and scoring?
5. What factors influence scheduling?
6. What are taints and tolerations?
7. What is node affinity?
8. Why do Pods remain in Pending state?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Scheduler selects worker nodes.
- Scheduler does not run containers.
- Scheduling uses filtering and scoring.
- Resource availability influences placement.
- Affinity and taints affect scheduling decisions.
- Pending Pods often indicate scheduling issues.
- Fundamental Kubernetes architecture topic.