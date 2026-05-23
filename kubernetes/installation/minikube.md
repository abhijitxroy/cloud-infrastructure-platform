# Minikube

## Overview

Minikube is a lightweight Kubernetes environment commonly used for local development, testing and learning purposes.

It provides a simplified way to run Kubernetes on a local workstation without provisioning a multi-node cluster.

Minikube is frequently used to explore Kubernetes concepts and validate workloads before larger environment deployment.

---

## Common Usage Areas

Examples:

- Kubernetes learning environments
- Local workload testing
- Manifest validation
- Application experimentation
- Development workflow validation

---

## Cluster Model

Production Kubernetes environments commonly run across multiple nodes.

Minikube provides a simplified local setup by running Kubernetes components on a local machine.

This approach helps reduce infrastructure setup effort for development and testing activities.

---

## Common Commands

Start cluster:

```bash
minikube start
```

Check status:

```bash
minikube status
```

List cluster nodes:

```bash
kubectl get nodes
```

List workloads:

```bash
kubectl get pods
```

Open dashboard:

```bash
minikube dashboard
```

---

## Notes

Minikube provides a practical environment for understanding Kubernetes concepts before working with larger infrastructure environments.