

# Node Selector

## Overview

Node Selector is the simplest Kubernetes scheduling mechanism used to place Pods on specific nodes.

It works by matching Pod requirements with node labels.

If a node contains the required label, the Pod can be scheduled there.

---

## Why Node Selector Matters

Without Node Selector:

```text
Scheduler
    ↓
Any Suitable Node
```

With Node Selector:

```text
Scheduler
    ↓
Node Label Match
    ↓
Specific Node
```

Benefits:

- Workload Isolation
- Hardware Targeting
- Environment Separation
- Simpler Scheduling

---

## How Node Selector Works

### Step 1

Node receives labels.

Example:

```text
environment=production
disk=ssd
region=india
```

---

### Step 2

Pod specifies Node Selector.

```text
environment=production
```

---

### Step 3

Scheduler searches for matching nodes.

---

### Step 4

Pod is scheduled on a matching node.

---

## Architecture

```text
Pod
 ↓
Node Selector
 ↓
environment=production
 ↓
Matching Node
```

---

## Common Use Cases

### Production Workloads

```text
environment=production
```

---

### SSD Storage Nodes

```text
disk=ssd
```

---

### GPU Workloads

```text
gpu=true
```

---

### Regional Placement

```text
region=india
```

---

## Node Selector vs Affinity

| Node Selector | Node Affinity |
| ------------- | ------------- |
| Simple Matching | Advanced Rules |
| Exact Label Match | Flexible Scheduling |
| No Preferences | Supports Preferences |
| Easy To Configure | More Powerful |

---

## Limitations

Node Selector:

```text
Supports Exact Matching Only
```

Does Not Support:

- Preferred Rules
- Complex Expressions
- Soft Constraints

For advanced scheduling use:

```text
Node Affinity
```

---

## Real Production Example

```text
GPU Nodes
     ↓
gpu=true
     ↓
ML Training Pods
```

Benefits:

- Efficient Resource Usage
- Hardware Isolation

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Missing Node Labels
- Incorrect Label Values
- Pods Stuck Pending
- Insufficient Matching Nodes

---

## Most Asked Interview Questions

1. What is Node Selector?
2. How does Node Selector work?
3. Node Selector vs Node Affinity?
4. Why would a Pod remain Pending?
5. What are common Node Selector use cases?
6. Can Node Selector use preferences?
7. How are node labels used?
8. When should Node Affinity be preferred?

---

## Quick Revision

### Priority

⭐⭐⭐⭐ High Priority

### Remember

- Node Selector is the simplest scheduling mechanism.
- It matches Pods with node labels.
- Supports exact matching only.
- Commonly used for workload isolation.
- Node Affinity is more flexible.
- Frequently asked Kubernetes scheduling topic.