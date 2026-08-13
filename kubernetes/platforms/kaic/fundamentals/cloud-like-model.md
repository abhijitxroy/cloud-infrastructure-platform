# KAIC Cloud-Like Model

## Internal Cloud

KAIC is moving toward an internal-cloud model that provides engineering teams with a cloud-like experience for consuming shared infrastructure.

The goal is to provide a single command-line interface through which users can create and manage different environments without needing to understand the underlying infrastructure implementation.

## Cloud-Like Experience

The user focuses on the required environment rather than the infrastructure steps needed to build it.

```text
User Requirement
       |
       v
    KAIC CLI
       |
       +-- VM configuration
       +-- Container configuration
       +-- Networking
       +-- Infrastructure provisioning
       +-- Environment configuration
       |
       v
Ready Environment
