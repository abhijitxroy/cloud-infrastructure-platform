# Kubelet

## Overview

Kubelet is the primary node agent that runs on each worker node in a Kubernetes cluster.

It is responsible for ensuring workloads assigned to a node are running as expected.

Kubelet continuously communicates with the Kubernetes Control Plane and helps maintain workload health.

---

## Responsibilities

Common responsibilities:

- Register worker nodes with the cluster
- Monitor Pod health
- Start containers
- Stop containers
- Report node status
- Maintain workload state

---

## Pod Management

Kubelet works with Pod specifications provided through Kubernetes APIs.

A Pod specification defines workload configuration requirements such as:

- Container image
- Resource configuration
- Environment variables
- Storage definitions

Kubelet ensures workloads running on the node align with expected configuration.

---

## Cluster Communication

Example interaction flow:

Control Plane

↓

API Server

↓

Kubelet

↓

Container Runtime

↓

Application Workload

---

## Notes

Kubelet is one of the core worker node components responsible for maintaining workload execution and node level operational stability.