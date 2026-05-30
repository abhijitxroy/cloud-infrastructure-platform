

# Kubectl Cheat Sheet

## Overview

Kubectl is the primary command-line tool used to interact with Kubernetes clusters.

It allows engineers to:

- Deploy Applications
- Inspect Resources
- Troubleshoot Issues
- Manage Clusters
- Perform Operational Tasks

---

## Why Kubectl Matters

Most Kubernetes administration tasks are performed using:

```text
kubectl
```

It is one of the most important tools for:

- Developers
- DevOps Engineers
- Platform Engineers
- Kubernetes Administrators

---

## Cluster Information

### Cluster Info

```bash
kubectl cluster-info
```

### Kubernetes Version

```bash
kubectl version
```

### View Nodes

```bash
kubectl get nodes
```

---

## Pod Commands

### List Pods

```bash
kubectl get pods
```

### List Pods In All Namespaces

```bash
kubectl get pods -A
```

### Describe Pod

```bash
kubectl describe pod <pod-name>
```

### Pod Logs

```bash
kubectl logs <pod-name>
```

### Execute Command Inside Pod

```bash
kubectl exec -it <pod-name> -- /bin/sh
```

### Delete Pod

```bash
kubectl delete pod <pod-name>
```

---

## Deployment Commands

### List Deployments

```bash
kubectl get deployments
```

### Describe Deployment

```bash
kubectl describe deployment <deployment-name>
```

### Scale Deployment

```bash
kubectl scale deployment <deployment-name> --replicas=5
```

### Restart Deployment

```bash
kubectl rollout restart deployment <deployment-name>
```

---

## Service Commands

### List Services

```bash
kubectl get svc
```

### Describe Service

```bash
kubectl describe svc <service-name>
```

---

## Namespace Commands

### List Namespaces

```bash
kubectl get namespaces
```

### Create Namespace

```bash
kubectl create namespace demo
```

---

## Apply And Delete Resources

### Create Or Update Resources

```bash
kubectl apply -f deployment.yaml
```

### Delete Resources

```bash
kubectl delete -f deployment.yaml
```

---

## Troubleshooting Commands

### Describe Resource

```bash
kubectl describe pod <pod-name>
```

### View Events

```bash
kubectl get events
```

### Resource Usage

```bash
kubectl top pods
kubectl top nodes
```

---

## Rollout Commands

### Rollout Status

```bash
kubectl rollout status deployment <deployment-name>
```

### Rollout History

```bash
kubectl rollout history deployment <deployment-name>
```

### Rollback

```bash
kubectl rollout undo deployment <deployment-name>
```

---

## Configuration Commands

### View Current Context

```bash
kubectl config current-context
```

### View Contexts

```bash
kubectl config get-contexts
```

### Switch Context

```bash
kubectl config use-context <context-name>
```

---

## Most Used Interview Commands

```bash
kubectl get pods
kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl exec -it <pod-name> -- /bin/sh
kubectl get svc
kubectl get deployments
kubectl get nodes
kubectl rollout restart deployment <deployment-name>
```

---

## Most Asked Interview Questions

1. What is kubectl?
2. How do you view Pods?
3. How do you check Pod logs?
4. How do you troubleshoot a failed Pod?
5. How do you scale a Deployment?
6. How do you restart a Deployment?
7. How do you access a Pod shell?
8. How do you perform a rollback?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Kubectl is the Kubernetes CLI.
- Used for deployment, management and troubleshooting.
- `get`, `describe`, `logs` and `exec` are the most commonly used commands.
- Essential tool for Kubernetes operations and interviews.