@'
# KAIC Architecture

## Overview

KAIC is designed as a unified infrastructure orchestration layer that provides a cloud-like experience for engineering teams.

The platform hides the underlying infrastructure complexity and provides a single CLI through which users can create and manage different environments.

## High-Level Architecture

```text
                         User
                           |
                           v
                      KAIC CLI
                           |
                           v
                  Environment Request
                           |
              +------------+------------+
              |            |            |
              v            v            v
           Define       Validate     Parameters
                           |
                           v
                       Schedule
                           |
                           v
                  Shared Infrastructure
                           |
             +-------------+-------------+
             |             |             |
             v             v             v
         Container         VM           OCP
                                        |
                                        v
                               OpenShift Cluster
