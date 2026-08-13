# KAIC Flavors

## Overview

KAIC uses a flavor-based resource selection model similar to cloud platforms.

A flavor represents a predefined resource or hardware profile that can be selected when creating an environment.

The purpose is to allow users to select an appropriate resource profile without needing to specify every underlying infrastructure detail.

## Resource Profile

A flavor can represent resources such as:

- CPU
- Memory
- Other supported resources
- Hardware or accelerator characteristics where applicable

Conceptually:

```text
User
  |
  | Select flavor
  v
KAIC
  |
  v
Predefined Resource / Hardware Profile
  |
  +-- CPU
  +-- Memory
  +-- Other supported resources
  