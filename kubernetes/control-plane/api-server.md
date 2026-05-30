# API Server

## Overview

The API Server is the central communication component of the Kubernetes Control Plane.

It acts as the entry point for cluster operations and processes requests related to Kubernetes resources.

Cluster components communicate with Kubernetes through the API Server.

---

## Responsibilities

Common responsibilities:

- Process API requests
- Validate configuration requests
- Update cluster state
- Coordinate communication between components
- Expose Kubernetes APIs

---

## Communication Flow

Example workflow:

User

↓

Kubectl

↓

API Server

↓

Control Plane Components

↓

Worker Nodes

The API Server helps maintain a consistent interface for interacting with the Kubernetes cluster.

---

## Examples

Operations commonly processed through the API Server:

- Create deployment
- Scale application
- Update configuration
- Query cluster resources
- Delete workloads

---

## Notes

Most Kubernetes management operations eventually flow through the API Server, making it one of the primary components of cluster management.
# API Server

## Overview

The API Server is the central communication component of the Kubernetes Control Plane.

It acts as the entry point for all cluster operations.

Every major Kubernetes component communicates through the API Server.

Examples:

- Kubectl
- Scheduler
- Controller Manager
- Kubelet
- External Tools

Without the API Server, cluster management operations cannot be performed.

---

## Why API Server Matters

The API Server provides:

- Centralized Access
- Authentication
- Authorization
- Request Validation
- Cluster State Management

It acts as the front door of Kubernetes.

---

## Architecture Position

```text
Users / CI-CD
       ↓
    Kubectl
       ↓
   API Server
       ↓
 ┌─────────────┐
 │    ETCD     │
 └─────────────┘
       ↑
Scheduler
Controller Manager
Kubelet
```

---

## Responsibilities

### API Processing

Processes requests such as:

- Create Pods
- Create Deployments
- Update Services
- Delete Resources

---

### Authentication

Verifies client identity.

Examples:

- Certificates
- Service Accounts
- Tokens

---

### Authorization

Determines whether a request is allowed.

Common Mechanism:

```text
RBAC
```

---

### Request Validation

Checks:

- Resource Definitions
- Configuration Syntax
- API Rules

Invalid requests are rejected.

---

### Cluster State Updates

Stores cluster state in ETCD.

Examples:

- Pods
- Deployments
- Services
- Nodes

---

## Request Flow

Example:

```text
kubectl apply deployment.yaml
            ↓
       API Server
            ↓
       Validation
            ↓
          ETCD
            ↓
        Scheduler
            ↓
         Kubelet
            ↓
          Pod
```

---

## Communication Model

Important Rule:

```text
Components Do Not
Directly Modify ETCD
```

Instead:

```text
Components
      ↓
API Server
      ↓
ETCD
```

---

## High Availability

Production clusters typically run:

```text
Multiple API Servers
         ↓
    Load Balancer
```

Benefits:

- Fault Tolerance
- High Availability
- Better Reliability

---

## Real Production Example

```text
Developer Deploys Application
             ↓
Kubectl Sends Request
             ↓
API Server Validates Request
             ↓
Deployment Stored In ETCD
             ↓
Scheduler Assigns Node
             ↓
Application Starts
```

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- API Server Unavailable
- Authentication Failures
- Authorization Errors
- ETCD Connectivity Issues
- High API Latency

---

## Most Asked Interview Questions

1. What is the Kubernetes API Server?
2. Why is it called the entry point of Kubernetes?
3. What are the responsibilities of the API Server?
4. How does the API Server interact with ETCD?
5. What is the role of authentication and authorization?
6. Why do Kubernetes components communicate through the API Server?
7. How is API Server high availability achieved?
8. What happens if the API Server becomes unavailable?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- API Server is the entry point of Kubernetes.
- All cluster operations flow through it.
- It handles authentication and authorization.
- It validates requests before storing state.
- ETCD is accessed through the API Server.
- Multiple API Servers are used in production.
- Fundamental Kubernetes architecture topic.