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