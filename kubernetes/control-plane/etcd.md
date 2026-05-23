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