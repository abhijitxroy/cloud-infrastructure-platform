

# CNI (Container Network Interface)

## Overview

CNI (Container Network Interface) is a networking specification used by Kubernetes to provide network connectivity for Pods.

CNI plugins are responsible for:

- Pod Networking
- IP Address Allocation
- Network Routing
- Inter-Node Communication

Without a CNI plugin, Pods cannot communicate with each other.

---

## Why CNI Matters

Kubernetes creates Pods.

CNI provides:

```text
Pod
 ↓
IP Address
 ↓
Network Connectivity
 ↓
Communication
```

CNI enables:

- Pod-to-Pod Communication
- Pod-to-Service Communication
- Cross-Node Networking
- Network Isolation

---

## Architecture

```text
Pod A
  ↓
CNI Plugin
  ↓
Network Layer
  ↓
CNI Plugin
  ↓
Pod B
```

---

## Responsibilities

### IP Allocation

Assigns IP addresses to Pods.

Example:

```text
Pod A → 10.244.1.5
Pod B → 10.244.2.8
```

---

### Network Routing

Routes traffic between:

- Pods
- Nodes
- Services

---

### Connectivity

Provides communication across:

- Same Node
- Different Nodes
- Entire Cluster

---

### Network Policies

Some CNI plugins support:

```text
NetworkPolicy
```

for traffic control and security.

---

## Popular CNI Plugins

### Calico

Features:

- Network Policies
- High Performance
- Production Ready

### Flannel

Features:

- Simple Setup
- Easy Learning
- Lightweight Networking

### Cilium

Features:

- eBPF Based Networking
- Advanced Security
- High Scalability

### Weave Net

Features:

- Simple Deployment
- Multi-Host Networking

---

## Pod Communication Example

```text
Pod A (Node 1)
        ↓
     CNI
        ↓
Cluster Network
        ↓
     CNI
        ↓
Pod B (Node 2)
```

---

## Real Production Example

```text
100 Worker Nodes
       ↓
5000 Pods
       ↓
CNI Provides Connectivity
       ↓
Applications Communicate
```

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Pod Connectivity Issues
- DNS Resolution Problems
- Network Policy Misconfiguration
- IP Exhaustion
- Cross-Node Communication Failures

---

## Most Asked Interview Questions

1. What is CNI?
2. Why does Kubernetes need CNI?
3. What problems does CNI solve?
4. What are popular CNI plugins?
5. Calico vs Flannel?
6. What is Cilium?
7. How do Pods communicate across nodes?
8. How do Network Policies work?

---

## Quick Revision

### Priority

⭐⭐⭐⭐ High Priority

### Remember

- CNI provides Kubernetes networking.
- Pods require CNI for communication.
- CNI handles IP allocation and routing.
- Calico, Flannel and Cilium are common plugins.
- Network Policies often depend on CNI support.
- Fundamental Kubernetes networking topic.