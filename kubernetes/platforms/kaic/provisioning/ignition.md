# KAIC Ignition Configuration

## Overview

Ignition configuration is part of the OpenShift worker-node provisioning workflow demonstrated in the KAIC session.

The recording states that after the OpenShift control plane becomes ready, KAIC obtains the worker Ignition configuration required to configure the worker nodes.

## Role in OCP Provisioning

The high-level flow is:

```text
Control Plane Ready
        |
        v
Worker Ignition Configuration
        |
        v
Worker Node Provisioning
        |
        v
Worker Node Configuration
        |
        v
Worker Connects to Cluster
