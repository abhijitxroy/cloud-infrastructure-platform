# KAIC OpenShift Provisioning

## Overview

The recorded KAIC session demonstrates the creation of a complete OpenShift environment through a single KAIC CLI command.

The demonstrated environment contains:

- 1 control plane node
- 4 worker nodes
- 5 nodes total

KAIC performs the underlying VM provisioning and OpenShift configuration required to produce the ready cluster.

## Demonstrated Command

```bash
./out/bin/kaic create ocp \
    --flavor g3 \
    --namespace admin \
    --image ocp4.22 \
    --ssh-key ~/.ssh/id_ed25519.pub \
    --replication 5
