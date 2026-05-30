

# Kubernetes Questions and Answers

## Overview

This document contains the most important Kubernetes questions frequently discussed in engineering interviews, production operations, platform engineering, and system design discussions.

The focus is on practical understanding rather than memorization.

---

# Kubernetes Fundamentals

## What is Kubernetes?

### Short Answer

Kubernetes is an open-source container orchestration platform used to deploy, manage, scale, and operate containerized applications.

### Production Example

A company running 500 microservices uses Kubernetes to automate deployment, scaling, self-healing, and service discovery.

---

## Why is Kubernetes needed when Docker already exists?

### Short Answer

Docker runs containers.

Kubernetes manages containers at scale.

### Production Example

Running one container on a laptop is easy.

Managing thousands of containers across hundreds of servers requires Kubernetes.

---

## What problems does Kubernetes solve?

### Short Answer

- Automated Deployment
- Scaling
- Self-Healing
- Service Discovery
- Load Balancing
- Resource Management

---

# Architecture

## What are the main Kubernetes components?

### Short Answer

Control Plane:

- API Server
- Scheduler
- Controller Manager
- etcd

Worker Node:

- Kubelet
- Kube Proxy
- Container Runtime

---

## Control Plane vs Worker Node?

| Control Plane | Worker Node |
| ------------ | ----------- |
| Makes Decisions | Runs Workloads |
| Cluster Management | Application Execution |
| Scheduler Runs Here | Pods Run Here |
| etcd Runs Here | Containers Run Here |

---

# Workloads

## What is a Pod?

### Short Answer

A Pod is the smallest deployable unit in Kubernetes.

A Pod can contain one or more containers.

### Production Example

A Java application container and a logging sidecar container running together.

---

## Deployment vs StatefulSet?

| Deployment | StatefulSet |
| ---------- | ----------- |
| Stateless Applications | Stateful Applications |
| Replaceable Pods | Stable Pod Identity |
| Web Applications | Databases |
| No Persistent Identity | Persistent Identity |

---

## Service vs Ingress?

| Service | Ingress |
| -------- | ------- |
| Internal Access | External Access |
| Pod Networking | HTTP/HTTPS Routing |
| Cluster Communication | Internet Traffic |
| Layer 4 | Layer 7 |

---

# Scheduling

## What is the Kubernetes Scheduler?

### Short Answer

The Scheduler selects the most suitable worker node for a Pod.

It considers:

- CPU
- Memory
- Affinity Rules
- Taints
- Resource Availability

---

## Affinity vs Taints?

### Short Answer

Affinity attracts Pods.

Taints repel Pods.

Tolerations allow exceptions.

---

# Security

## What is RBAC?

### Short Answer

RBAC (Role-Based Access Control) controls what users and workloads can do inside a Kubernetes cluster.

### Remember

Authentication:

```text
Who Are You?
```

Authorization:

```text
What Can You Do?
```

---

## What is a Service Account?

### Short Answer

A Service Account provides an identity for workloads running inside Kubernetes.

Pods use Service Accounts when accessing the Kubernetes API.

---

## Network Policies vs RBAC?

| Network Policies | RBAC |
| ---------------- | ---- |
| Controls Network Traffic | Controls API Access |
| Pod Communication | User Permissions |
| Network Security | Authorization |

---

# Storage

## PV vs PVC vs StorageClass?

| Component | Responsibility |
| ---------- | ------------- |
| StorageClass | Creates Storage |
| Persistent Volume | Provides Storage |
| Persistent Volume Claim | Requests Storage |

### Easy Flow

```text
Application
      ↓
PVC
      ↓
StorageClass
      ↓
PV
      ↓
Storage Backend
```

---

# Operations

## How do you troubleshoot a failed Pod?

### Common Approach

```text
kubectl get pods
        ↓
kubectl describe pod
        ↓
kubectl logs
        ↓
kubectl get events
        ↓
Root Cause Analysis
```

---

## What is CrashLoopBackOff?

### Short Answer

The container starts, crashes, restarts, and repeatedly fails.

Common Causes:

- Application Errors
- Missing Configuration
- Dependency Failures

---

## What is ImagePullBackOff?

### Short Answer

Kubernetes cannot download the container image.

Common Causes:

- Invalid Image Name
- Registry Authentication Issues
- Network Problems

---

# Quick Revision

## Must Know Topics

- Pod
- Deployment
- Service
- Ingress
- StatefulSet
- Scheduler
- Affinity
- Taints and Tolerations
- RBAC
- Service Accounts
- Network Policies
- PV, PVC, StorageClass
- Kubelet
- Kube Proxy
- Container Runtime
- Troubleshooting

These topics cover the majority of Kubernetes discussions in engineering interviews and production environments.