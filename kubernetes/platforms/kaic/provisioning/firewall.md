# KAIC Firewall Configuration

## Overview

Firewall configuration is part of the OpenShift provisioning workflow demonstrated in the KAIC session.

KAIC configures the control-plane firewall so that newly provisioned worker nodes can connect to the OpenShift cluster.

## Purpose

The recorded session explicitly describes configuring the control-plane firewall to allow new worker nodes to connect to the cluster.

```text
Worker Node
     |
     | Required cluster connectivity
     v
Control-Plane Firewall
     |
     | Allowed traffic
     v
Control Plane
