# Rolling Update

## Overview

Rolling update is a deployment strategy used to update application workloads gradually without replacing all running instances at the same time.

Kubernetes supports rolling updates to help reduce service disruption during application deployment.

This approach allows workload changes while maintaining application availability.

---

## Update Flow

Example workflow:

Current Version

Application v1

↓

Deployment Update

↓

Gradual Pod Replacement

↓

Application v2

Kubernetes updates workloads incrementally until the deployment reaches the expected state.

---

## Operational Benefits

Rolling updates help improve:

- Application availability
- Deployment reliability
- Controlled rollout process
- Operational stability

---

## Rollback Support

If issues are detected during deployment, Kubernetes supports rollback capabilities to restore previously stable application versions.

Rollback helps reduce deployment related operational risk.

---

## Kubernetes Components Involved

Examples:

- Deployment
- ReplicaSet
- Pod

These components work together to coordinate workload updates.

---

## Notes

Rolling update capability is an important operational feature for managing application delivery in containerized environments while reducing service interruption.
# Rolling Update

## Overview

A Rolling Update is a Kubernetes deployment strategy that gradually replaces old application Pods with new Pods.

The update occurs incrementally instead of replacing all Pods at the same time.

This helps maintain application availability during deployments.

---

## Why Rolling Updates Matter

Without Rolling Updates:

```text
Version 1 Pods Stopped
          ↓
Downtime
          ↓
Version 2 Pods Started
```

With Rolling Updates:

```text
Version 1 Pods
      ↓
Version 1 + Version 2 Pods
      ↓
Version 2 Pods
```

Benefits:

- Zero Or Minimal Downtime
- Safer Releases
- Easier Validation
- Better Reliability

---

## Rolling Update Flow

```text
Deployment Update
        ↓
New Pod Created
        ↓
Health Check Passes
        ↓
Old Pod Removed
        ↓
Repeat Process
        ↓
Deployment Complete
```

---

## Kubernetes Components Involved

```text
Deployment
     ↓
ReplicaSet
     ↓
Pods
```

Responsibilities:

- Deployment controls rollout strategy.
- ReplicaSets manage old and new versions.
- Pods run application containers.

---

## Example Deployment

Initial State:

```text
v1 Pod
v1 Pod
v1 Pod
```

During Update:

```text
v1 Pod
v1 Pod
v2 Pod
```

Final State:

```text
v2 Pod
v2 Pod
v2 Pod
```

---

## Rollback Support

If issues are detected:

```text
Version 2 Deployment
         ↓
Issue Detected
         ↓
Rollback
         ↓
Version 1 Deployment
```

Benefits:

- Faster Recovery
- Reduced Deployment Risk
- Safer Production Releases

---

## Update Strategy Parameters

### maxUnavailable

Controls how many Pods can be unavailable during updates.

---

### maxSurge

Controls how many additional Pods can be created during updates.

---

## Real Production Example

```text
E-Commerce Application
          ↓
10 Running Pods
          ↓
Application Upgrade
          ↓
Pods Replaced Gradually
          ↓
No Customer Downtime
```

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Failed Rollouts
- Readiness Probe Failures
- Image Pull Errors
- Insufficient Resources
- Stuck Deployments

---

## Most Asked Interview Questions

1. What is a Rolling Update?
2. Why are Rolling Updates used?
3. How do Rolling Updates avoid downtime?
4. What is the role of a Deployment?
5. What is maxSurge?
6. What is maxUnavailable?
7. How do rollbacks work?
8. Rolling Update vs Recreate strategy?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Rolling Updates replace Pods gradually.
- They help minimize downtime.
- Deployments manage rolling updates.
- Rollbacks allow quick recovery.
- maxSurge and maxUnavailable control rollout behavior.
- One of the most important Kubernetes deployment topics.