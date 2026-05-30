

# Namespace

## Overview

A Namespace is a Kubernetes resource used to logically separate workloads and resources within a cluster.

Namespaces help organize applications, teams, environments, and access controls.

They provide isolation without requiring separate Kubernetes clusters.

---

## Why Namespaces Matter

Without Namespaces:

```text
Single Cluster
      ↓
All Resources Mixed Together
```

With Namespaces:

```text
Cluster
 ├── dev
 ├── test
 ├── staging
 └── production
```

Benefits:

- Better Organization
- Environment Separation
- Resource Isolation
- Access Control
- Easier Management

---

## Architecture

```text
Kubernetes Cluster
        ↓
 ┌─────────────┐
 │ dev         │
 │ test        │
 │ production  │
 └─────────────┘
```

Resources inside one namespace are logically separated from resources in another namespace.

---

## Common Use Cases

### Environment Separation

```text
Development
Testing
Production
```

---

### Team Separation

```text
Frontend Team
Backend Team
Platform Team
```

---

### Multi-Tenant Clusters

```text
Team A Namespace
Team B Namespace
Team C Namespace
```

---

## Default Namespaces

### default

Used when no namespace is specified.

---

### kube-system

Stores Kubernetes system components.

Examples:

- CoreDNS
- API Server Components
- Controllers

---

### kube-public

Publicly readable cluster information.

---

### kube-node-lease

Used for node heartbeat management.

---

## Namespace Commands

List Namespaces:

```bash
kubectl get namespaces
```

Create Namespace:

```bash
kubectl create namespace dev
```

View Resources:

```bash
kubectl get pods -n dev
```

---

## Namespace vs Cluster

| Namespace | Cluster |
| ---------- | ------- |
| Logical Isolation | Physical/Administrative Boundary |
| Shared Infrastructure | Separate Infrastructure |
| Lower Cost | Higher Cost |
| Easier Management | Stronger Isolation |

---

## Real Production Example

```text
production
 ├── frontend
 ├── backend
 └── database

staging
 ├── frontend
 ├── backend
 └── database
```

Both environments run in the same cluster while remaining logically separated.

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Wrong Namespace Usage
- Resource Visibility Issues
- RBAC Permission Problems
- Deployment To Incorrect Namespace
- Resource Quota Restrictions

---

## Most Asked Interview Questions

1. What is a Kubernetes Namespace?
2. Why are Namespaces needed?
3. What are the default namespaces?
4. Namespace vs Cluster?
5. How do Namespaces improve isolation?
6. How do you deploy resources into a namespace?
7. How does RBAC interact with Namespaces?
8. When should separate clusters be used instead of namespaces?

---

## Quick Revision

### Priority

⭐⭐⭐⭐ High Priority

### Remember

- Namespaces provide logical isolation.
- Namespaces help organize workloads.
- Commonly used for dev, test and production environments.
- RBAC is frequently applied at namespace level.
- Multiple teams can share a cluster using namespaces.
- Frequently asked Kubernetes administration topic.