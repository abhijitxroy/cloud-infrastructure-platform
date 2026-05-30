

# DaemonSet

## Overview

A DaemonSet is a Kubernetes workload object that ensures a Pod runs on every worker node in a cluster.

As new nodes are added, Kubernetes automatically creates DaemonSet Pods on those nodes.

As nodes are removed, the associated Pods are removed as well.

DaemonSets are commonly used for cluster-wide infrastructure services.

---

## Why DaemonSets Matter

Normal workloads:

```text
Deployment
     ↓
Selected Nodes
```

DaemonSet:

```text
DaemonSet
      ↓
Every Worker Node
```

Benefits:

- Cluster-Wide Coverage
- Automatic Node Onboarding
- Consistent Operations
- Simplified Infrastructure Management

---

## Architecture

```text
DaemonSet
      ↓
Node 1 → Pod
Node 2 → Pod
Node 3 → Pod
Node 4 → Pod
```

One Pod runs on each node.

---

## Common Use Cases

### Log Collection

Examples:

- Fluentd
- Fluent Bit
- Filebeat

---

### Monitoring Agents

Examples:

- Node Exporter
- Datadog Agent
- New Relic Agent

---

### Security Agents

Examples:

- Falco
- Security Monitoring Tools

---

### Networking Components

Examples:

- CNI Agents
- Network Monitoring Tools

---

## DaemonSet Behavior

### New Node Added

```text
New Worker Node
        ↓
DaemonSet Detects Node
        ↓
Pod Automatically Created
```

---

### Node Removed

```text
Node Removed
      ↓
DaemonSet Pod Removed
```

---

## DaemonSet vs Deployment

| DaemonSet | Deployment |
| ---------- | ---------- |
| One Pod Per Node | Configurable Replica Count |
| Infrastructure Workloads | Application Workloads |
| Runs On All Nodes | Runs On Selected Nodes |
| Cluster Services | Business Services |

---

## Real Production Example

```text
100 Worker Nodes
        ↓
Node Exporter DaemonSet
        ↓
100 Monitoring Pods
```

Result:

```text
Every Node Monitored
```

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Missing DaemonSet Pods
- Node Selector Issues
- Resource Constraints
- Agent Startup Failures
- Node Scheduling Problems

---

## Most Asked Interview Questions

1. What is a DaemonSet?
2. Why are DaemonSets needed?
3. DaemonSet vs Deployment?
4. What workloads typically use DaemonSets?
5. What happens when a new node is added?
6. How are monitoring agents deployed?
7. How are logging agents deployed?
8. What is a real-world DaemonSet example?

---

## Quick Revision

### Priority

⭐⭐⭐⭐ High Priority

### Remember

- DaemonSets run one Pod on every node.
- New nodes automatically receive DaemonSet Pods.
- Commonly used for monitoring, logging, networking and security.
- DaemonSets are infrastructure-focused workloads.
- Frequently asked Kubernetes operations topic.