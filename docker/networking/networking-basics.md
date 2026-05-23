# Networking Basics

## Overview

Docker networking enables communication between containers, external systems and application services.

Networking capabilities help containerized applications interact while maintaining workload isolation and operational flexibility.

Docker provides networking mechanisms that support different deployment requirements.

---

## Common Network Types

### Bridge Network

Default Docker networking model commonly used for communication between containers running on the same host.

### Host Network

Containers share networking resources directly with the host environment.

### None Network

Container runs without external network connectivity.

### Overlay Network

Supports communication across distributed container environments.

---

## Container Communication

Examples:

- Container to container communication
- Container to host communication
- Container to external service communication

Networking configuration influences application connectivity and deployment architecture.

---

## Operational Considerations

Networking design commonly includes:

- Service communication
- DNS resolution
- Port exposure
- Traffic isolation
- Connectivity management

---

## Port Mapping

Applications commonly expose services through port mapping.

Example:

Application

↓

Container Port

↓

Host Port

↓

External Access

---

## Notes

Container networking plays an important role in application deployment models and distributed infrastructure environments.