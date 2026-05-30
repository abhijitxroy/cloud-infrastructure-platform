

# Probes

## Overview

Probes are Kubernetes health checks used to determine the status of containers running inside Pods.

Kubernetes supports three probe types:

- Liveness Probe
- Readiness Probe
- Startup Probe

Probes help Kubernetes automatically detect unhealthy applications and take corrective actions.

---

## Why Probes Matter

Without Probes:

```text
Application Hangs
        ↓
Still Appears Running
        ↓
Users Experience Failures
```

With Probes:

```text
Application Problem
        ↓
Probe Detects Issue
        ↓
Kubernetes Responds
```

Benefits:

- Self Healing
- Better Availability
- Faster Recovery
- Improved Reliability

---

## Probe Types

### Liveness Probe

Determines whether a container is alive.

If the probe fails:

```text
Container Restarted
```

Use Cases:

- Deadlocks
- Hung Processes
- Unresponsive Applications

---

### Readiness Probe

Determines whether a container is ready to receive traffic.

If the probe fails:

```text
Pod Removed From Service Endpoints
```

The container continues running.

Use Cases:

- Application Startup
- Database Connectivity
- Dependency Availability

---

### Startup Probe

Used for slow-starting applications.

During startup:

```text
Startup Probe Active
        ↓
Liveness And Readiness Delayed
```

Use Cases:

- Large Java Applications
- Databases
- Legacy Applications

---

## Probe Flow

```text
Container Starts
        ↓
Startup Probe
        ↓
Readiness Probe
        ↓
Traffic Allowed
        ↓
Liveness Probe
        ↓
Continuous Health Monitoring
```

---

## Probe Methods

### HTTP Probe

Checks an HTTP endpoint.

Example:

```text
/health
/ready
```

---

### TCP Probe

Checks whether a port is accepting connections.

---

### Command Probe

Executes a command inside the container.

Example:

```text
cat /tmp/healthy
```

---

## Real Production Example

```text
Spring Boot Application
          ↓
Startup Probe
          ↓
Application Initialization
          ↓
Readiness Probe
          ↓
Traffic Enabled
          ↓
Liveness Probe
          ↓
Automatic Recovery
```

---

## Common Misconfigurations

- Aggressive Timeouts
- Incorrect Health Endpoints
- Missing Startup Probe
- Readiness Returning Success Too Early
- Liveness Restart Loops

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- CrashLoopBackOff
- Unhealthy Pods
- Traffic Routing Problems
- Startup Delays
- Repeated Container Restarts

---

## Most Asked Interview Questions

1. What are Kubernetes Probes?
2. Liveness vs Readiness Probe?
3. What is a Startup Probe?
4. When should Startup Probes be used?
5. What happens when a Liveness Probe fails?
6. What happens when a Readiness Probe fails?
7. HTTP vs TCP vs Command Probes?
8. How do Probes improve reliability?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Liveness checks if the container is alive.
- Readiness checks if traffic should be routed.
- Startup handles slow-starting applications.
- Failed Liveness causes restart.
- Failed Readiness removes traffic.
- Probes are fundamental for production Kubernetes workloads.