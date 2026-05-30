

# Pod Lifecycle

## Overview

The Pod Lifecycle describes the different phases a Pod goes through from creation to termination.

Understanding Pod lifecycle states is essential for troubleshooting Kubernetes workloads and production incidents.

---

## Why Pod Lifecycle Matters

Every Kubernetes workload runs inside Pods.

Understanding lifecycle states helps engineers:

- Troubleshoot Failures
- Diagnose Scheduling Problems
- Investigate Startup Issues
- Monitor Application Health
- Debug Production Incidents

---

## Lifecycle Flow

```text
Pending
   ↓
Container Creating
   ↓
Running
   ↓
Succeeded / Failed
   ↓
Terminated
```

---

## Pod Phases

### Pending

The Pod has been accepted by Kubernetes but is not yet running.

Common Reasons:

- Node Not Available
- Image Pull In Progress
- Resource Constraints
- Scheduling Delays

---

### Running

The Pod has been scheduled and at least one container is running.

```text
Pod Ready
      ↓
Serving Traffic
```

---

### Succeeded

All containers completed successfully.

Common For:

- Jobs
- Batch Processing
- Data Migration Tasks

---

### Failed

One or more containers terminated unsuccessfully.

Common Reasons:

- Application Crash
- Configuration Issues
- Dependency Failures

---

### Unknown

Kubernetes cannot determine the Pod state.

Usually caused by:

- Node Communication Problems
- Kubelet Issues

---

## Container States

### Waiting

Container is preparing to start.

Examples:

- ImagePullBackOff
- ErrImagePull
- ContainerCreating

---

### Running

Container is executing normally.

---

### Terminated

Container has stopped.

Possible Outcomes:

- Success
- Failure

---

## Common Failure States

### CrashLoopBackOff

```text
Container Starts
       ↓
Container Crashes
       ↓
Restart
       ↓
Crash Again
```

One of the most common production issues.

---

### ImagePullBackOff

Kubernetes cannot pull the container image.

Common Causes:

- Wrong Image Name
- Authentication Problems
- Registry Connectivity Issues

---

### Pending Forever

Common Causes:

- Insufficient CPU
- Insufficient Memory
- Scheduling Constraints

---

## Pod Termination Flow

```text
Termination Requested
         ↓
SIGTERM Sent
         ↓
Grace Period
         ↓
Container Stops
         ↓
Pod Removed
```

---

## Real Production Example

```text
Deployment Updated
        ↓
Old Pod Terminated
        ↓
New Pod Created
        ↓
Running
        ↓
Ready
```

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- CrashLoopBackOff
- ImagePullBackOff
- Pending Pods
- Startup Failures
- Readiness Issues

---

## Most Asked Interview Questions

1. What is the Pod lifecycle?
2. What are the Pod phases?
3. What is CrashLoopBackOff?
4. What is ImagePullBackOff?
5. Why does a Pod remain Pending?
6. Difference between Pod phase and container state?
7. What happens during Pod termination?
8. How do you troubleshoot failed Pods?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Pending → Running → Succeeded/Failed.
- Containers have Waiting, Running and Terminated states.
- CrashLoopBackOff is a common production issue.
- ImagePullBackOff indicates image retrieval problems.
- Pod lifecycle knowledge is critical for troubleshooting.