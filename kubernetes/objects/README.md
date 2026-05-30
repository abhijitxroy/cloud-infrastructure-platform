# Objects

Core Kubernetes resources and deployment building blocks.
# Objects

## Overview

Kubernetes Objects are persistent resources used to represent workloads, networking, configuration, scheduling, and application state inside a Kubernetes cluster.

Objects define the desired state that Kubernetes continuously maintains.

---

## Why Objects Matter

Kubernetes is built around objects.

Examples:

- Pods
- Deployments
- Services
- ConfigMaps
- Secrets
- StatefulSets
- DaemonSets
- Jobs
- Ingress

These objects allow Kubernetes to automate application management.

---

## Topics

### Workload Objects

- Pod
- Deployment
- StatefulSet
- DaemonSet
- Job and CronJob

### Networking Objects

- Service
- Ingress

### Configuration Objects

- ConfigMap
- Secret

---

## Object Relationships

```text
Ingress
   ↓
Service
   ↓
Deployment
   ↓
ReplicaSet
   ↓
Pods
```

Configuration:

```text
ConfigMap
      ↓
Application

Secret
      ↓
Application
```

---

## Learning Path

```text
Pod
 ↓
Deployment
 ↓
Service
 ↓
Ingress
 ↓
ConfigMap
 ↓
Secret
 ↓
StatefulSet
 ↓
Advanced Workloads
```

---

## Related Sections

- Fundamentals
- Architecture
- Networking
- Storage
- Security
- Operations

---

## Most Asked Interview Questions

1. What are Kubernetes Objects?
2. What is the difference between Pod and Deployment?
3. Why are Services required?
4. ConfigMap vs Secret?
5. Deployment vs StatefulSet?
6. DaemonSet vs Deployment?
7. What is Ingress?
8. How do Kubernetes objects work together?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Kubernetes manages everything through objects.
- Pods are the smallest deployable unit.
- Deployments manage stateless workloads.
- StatefulSets manage stateful workloads.
- Services provide stable networking.
- ConfigMaps and Secrets manage configuration.
- Objects are fundamental to Kubernetes operations.