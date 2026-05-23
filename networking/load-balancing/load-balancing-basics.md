# Load Balancing Basics

## Overview

Load balancing distributes incoming traffic across multiple application instances or infrastructure resources.

It helps improve application availability, operational stability and resource utilization.

Load balancing becomes increasingly important as infrastructure environments scale and application demand changes over time.

---

## Common Objectives

Load balancing commonly supports:

- Traffic distribution
- High availability
- Fault tolerance
- Scalability
- Resource optimization

---

## Traffic Flow

Example workflow:

Client Request

↓

Load Balancer

↓

Application Instance 1

or

Application Instance 2

or

Application Instance 3

Traffic distribution helps prevent workloads from concentrating on a single infrastructure component.

---

## Common Load Balancing Models

### Layer 4 Load Balancing

Traffic routing based on transport layer information.

Examples:

- TCP
- UDP

---

### Layer 7 Load Balancing

Traffic routing based on application layer information.

Examples:

- HTTP routing
- URL path routing
- Host based routing

---

## Operational Benefits

Load balancing helps improve:

- Application availability
- Infrastructure resilience
- Traffic management
- Operational flexibility

---

## Common Infrastructure Usage

Examples:

- Cloud platforms
- Kubernetes environments
- Web applications
- API infrastructure

---

## Notes

Load balancing plays an important role in distributed systems where workload demand, resilience and scalability requirements evolve over time.