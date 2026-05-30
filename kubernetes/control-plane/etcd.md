# ETCD

## Overview

ETCD is the distributed key-value data store used by Kubernetes to maintain cluster information.

It acts as the source of truth for cluster state and stores information required for Kubernetes operations.

---

## Responsibilities

Common responsibilities:

- Store cluster configuration
- Maintain resource information
- Persist cluster state
- Support Control Plane operations

---

## Examples of Stored Information

Examples include:

- Pod information
- Deployment configuration
- Service definitions
- Cluster metadata
- Node information

---

## Cluster Interaction

Kubernetes Control Plane components retrieve and update information through ETCD.

Example flow:

API Server

↓

ETCD

↓

Cluster State Information

---

## Notes

ETCD plays an important role in cluster reliability because Kubernetes components depend on consistent cluster state information to operate correctly.
# ETCD

## Overview

ETCD is a distributed key-value database used by Kubernetes to store cluster state.

It acts as the single source of truth for the entire cluster.

Everything Kubernetes manages is ultimately stored in ETCD.

Examples:

- Pods
- Deployments
- Services
- ConfigMaps
- Secrets
- Nodes

Without ETCD, Kubernetes cannot maintain cluster state.

---

## Why ETCD Matters

Kubernetes depends on ETCD for:

- Configuration Storage
- Cluster State Management
- Service Discovery Information
- Resource Metadata
- Recovery Operations

ETCD is one of the most critical components of the Control Plane.

---

## Architecture Position

```text
Kubectl
    ↓
API Server
    ↓
ETCD
    ↓
Cluster State
```

Important:

```text
All State Changes
      ↓
Flow Through
      ↓
API Server
      ↓
ETCD
```

---

## Responsibilities

### Store Cluster State

Stores:

- Pods
- Deployments
- Services
- Nodes
- Namespaces

---

### Configuration Storage

Stores:

- Cluster Configuration
- Resource Definitions
- Metadata

---

### State Persistence

Ensures Kubernetes state survives:

- API Server Restarts
- Controller Restarts
- Node Failures

---

### Coordination

Provides consistent cluster information to Control Plane components.

---

## Data Examples

Typical Information Stored:

```text
Deployment
Replicas = 5
```

```text
Service
ClusterIP = 10.0.0.10
```

```text
Node
Status = Ready
```

---

## Communication Model

Important Rule:

```text
Components Do Not
Directly Update ETCD
```

Instead:

```text
Components
      ↓
API Server
      ↓
ETCD
```

This ensures:

- Validation
- Security
- Consistency

---

## Backup And Recovery

ETCD backup is one of the most important Kubernetes operational tasks.

Why?

```text
ETCD Lost
    ↓
Cluster State Lost
```

Production Recommendation:

```text
Regular ETCD Backups
```

---

## High Availability

Production clusters commonly run:

```text
ETCD Cluster
      ↓
Multiple Members
```

Benefits:

- Fault Tolerance
- Reliability
- Data Availability

---

## Real Production Example

```text
Developer Creates Deployment
            ↓
API Server Receives Request
            ↓
Deployment Stored In ETCD
            ↓
Scheduler Reads State
            ↓
Pods Created
```

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- ETCD Latency
- Cluster State Corruption
- Backup Failures
- Storage Exhaustion
- Control Plane Availability Issues

---

## Most Asked Interview Questions

1. What is ETCD?
2. Why is ETCD important in Kubernetes?
3. What information is stored in ETCD?
4. Is ETCD a database?
5. How does ETCD interact with the API Server?
6. Why are ETCD backups important?
7. What happens if ETCD becomes unavailable?
8. How is ETCD deployed in production?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- ETCD is the Kubernetes database.
- ETCD stores cluster state.
- ETCD is the source of truth.
- Components access ETCD through the API Server.
- ETCD backup is critical for disaster recovery.
- Production clusters use highly available ETCD deployments.
- Fundamental Kubernetes architecture topic.