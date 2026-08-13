# KAIC Lifecycle Management

## Overview

KAIC is designed to provide a unified CLI for managing the lifecycle of environments created on shared infrastructure.

The recorded session describes lifecycle operations for environments such as containers, virtual machines, and OpenShift environments.

## Lifecycle Operations

The session mentions the following lifecycle operations:

- Create
- Update
- Status
- Restart / reboot
- Shell
- Remove

Conceptually:

```text
                    KAIC Environment
                           |
          +----------------+----------------+
          |        |       |       |        |
          v        v       v       v        v
        Create   Update  Status  Restart  Remove
                                    |
                                    v
                                  Shell
