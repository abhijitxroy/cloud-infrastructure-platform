# KAIC Certificate Handling

## Overview

Certificate handling is part of the OpenShift worker-node provisioning workflow demonstrated in the KAIC session.

After the OpenShift control plane becomes ready, KAIC starts a certificate-approval process for certificates coming from incoming worker nodes.

## Position in the OCP Provisioning Workflow

```text
Control Plane Ready
        |
        v
Certificate Approval
        |
        +-- Worker Certificate
        |
        v
Worker Allowed to Connect
