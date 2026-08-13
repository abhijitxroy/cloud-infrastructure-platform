# KAIC Networking

## Overview

Networking is one of the infrastructure areas that KAIC abstracts from the end user.

The recorded session explains that users should not need to manually configure how VMs, containers, and other components are connected through networking.

For complex environments such as OpenShift, networking configuration is part of the automated environment-creation process.

## Networking in the KAIC Model

```text
User
  |
  | Environment Requirements
  v
KAIC
  |
  +-- Provisioning
  +-- Networking
  +-- DNS
  +-- Firewall
  +-- Environment Configuration
  |
  v
Ready Environment
