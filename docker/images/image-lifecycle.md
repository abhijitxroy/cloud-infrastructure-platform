# Image Lifecycle

## Overview

Docker images are immutable packaged artifacts that contain everything required to run an application.

Images commonly include:

- Application code
- Runtime dependencies
- Libraries
- Configuration
- Base operating system components

Containers are created from images during application execution.

---

## Image Build Flow

Example workflow:

Application Code

↓

Dockerfile

↓

Docker Build

↓

Docker Image

↓

Container Registry

↓

Container Runtime

↓

Running Container

---

## Image Characteristics

Container images provide:

- Consistent runtime environments
- Versioned application packaging
- Repeatable deployment behavior
- Environment portability

Images remain unchanged after creation. Application changes commonly require creation of a new image version.

---

## Layer Model

Docker images are built using layers.

Examples:

- Base image layer
- Dependency installation layer
- Application layer

Layer reuse helps improve build efficiency and storage optimization.

---

## Operational Considerations

Image lifecycle management commonly includes:

- Build process
- Version management
- Registry storage
- Security validation
- Deployment workflow integration

---

## Notes

Image standardization helps improve deployment consistency across infrastructure environments and delivery workflows.