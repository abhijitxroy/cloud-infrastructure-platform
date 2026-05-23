# Docker vs Kubernetes

## Docker

Docker focuses on container creation and container execution.

Common responsibilities:

- Build container images
- Run containers
- Package application dependencies
- Provide runtime environment consistency

Docker simplifies application deployment by reducing environment related differences across systems.

---

## Kubernetes

Kubernetes focuses on container orchestration and workload management.

Common responsibilities:

- Scaling workloads
- Service discovery
- Load balancing
- Self healing
- Rolling updates
- Configuration and secret handling

Kubernetes helps manage containerized applications when deployment environments grow larger and operational requirements become more complex.

---

## Container Runtime

Kubernetes interacts with container runtimes through the Container Runtime Interface (CRI).

Examples:

- containerd
- CRI-O

Container runtimes are responsible for starting and managing containers on worker nodes.

---

## OCI

Open Container Initiative (OCI) defines standards around container image and runtime specifications.

OCI compliance helps improve portability across container ecosystems.