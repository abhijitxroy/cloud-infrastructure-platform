# KAIC Overview

## What is KAIC?

KAIC is a tool designed to provide a cloud-like experience for engineering teams by exposing a unified command-line interface (CLI) for creating and managing different environments on shared infrastructure.

The core idea presented in the session is to hide infrastructure complexity from the end user.

The user should not need to understand how the underlying VMs, containers, networking, or other infrastructure components are configured and connected. Instead, the user defines the environment they need and KAIC performs the required infrastructure operations.

## Internal Cloud Concept

The session describes KAIC as moving toward an internal-cloud model:

```text
User
  |
  | Simple CLI command
  v
KAIC
  |
  +-- Infrastructure provisioning
  +-- Networking
  +-- Configuration
  +-- Environment creation
  |
  v
Ready Environment
