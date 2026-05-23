# Ingress

## Overview

Ingress is a Kubernetes resource used to manage external access to services running inside a cluster.

It provides routing capabilities that allow external traffic to reach application workloads through defined rules.

Ingress commonly works with HTTP and HTTPS traffic.

---

## Responsibilities

Common responsibilities:

- External traffic routing
- Path based routing
- Host based routing
- TLS termination
- Centralized traffic entry management

---

## Traffic Flow

Example workflow:

External Client

↓

Ingress

↓

Kubernetes Service

↓

Application Pods

Ingress provides a controlled entry point for traffic entering Kubernetes environments.

---

## Routing Examples

Examples:

- Route traffic based on application path
- Route traffic based on domain name
- Direct requests to different backend services

---

## Ingress and Egress

Ingress:

- Incoming traffic entering workloads

Egress:

- Outgoing traffic leaving workloads

These concepts are commonly used while designing communication patterns inside distributed systems.

---

## Notes

Ingress simplifies external application exposure and helps improve traffic management for Kubernetes based workloads.