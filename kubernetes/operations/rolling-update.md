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