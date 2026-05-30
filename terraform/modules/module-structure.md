

# Module Structure

## Overview

Module Structure defines how Terraform modules are organized to improve maintainability, reusability, scalability, and team collaboration.

A consistent module structure makes infrastructure easier to understand, maintain, test, and reuse across environments.

---

## Why Module Structure Matters

Without Structure:

```text
Terraform Code
       ↓
Mixed Responsibilities
       ↓
Maintenance Problems
```

With Structure:

```text
Well Defined Module
        ↓
Reusable Infrastructure
        ↓
Consistent Deployments
```

Benefits:

- Better Reusability
- Easier Maintenance
- Improved Governance
- Faster Development

---

## Recommended Module Structure

```text
module/
├── main.tf
├── variables.tf
├── outputs.tf
├── versions.tf
└── README.md
```

---

## main.tf

Contains:

- Resources
- Data Sources
- Core Infrastructure Logic

Purpose:

```text
Infrastructure Definition
```

---

## variables.tf

Defines module inputs.

Examples:

- Environment Name
- Resource Names
- CIDR Blocks
- Instance Types

Benefits:

- Flexibility
- Reusability

---

## outputs.tf

Exports values from the module.

Examples:

- VPC ID
- Subnet IDs
- Load Balancer DNS

Outputs allow modules to communicate.

---

## versions.tf

Defines:

- Terraform Version
- Provider Versions

Benefits:

- Predictable Deployments
- Upgrade Safety

---

## README.md

Documents:

- Purpose
- Inputs
- Outputs
- Usage Examples

Good documentation improves adoption and maintenance.

---

## Module Design Principles

### Single Responsibility

Each module should solve one problem.

Examples:

```text
VPC Module
EKS Module
RDS Module
```

Avoid combining unrelated infrastructure.

---

### Reusability

Design modules to work across environments.

Examples:

```text
Development
Staging
Production
```

---

### Configurability

Prefer variables instead of hardcoded values.

---

### Minimal Dependencies

Reduce tight coupling between modules.

---

## Real Production Example

```text
Networking Module
       ↓
VPC
Subnets
Route Tables
```

Used by:

```text
Dev
Stage
Prod
```

through variable-based configuration.

---

## Production Engineering Perspective

### Common Problems

- Hardcoded Values
- Large Monolithic Modules
- Missing Documentation
- Tight Coupling
- Poor Version Management

---

## Most Asked Interview Questions

1. What is a Terraform module structure?
2. What belongs in main.tf?
3. Why use variables.tf?
4. Why use outputs.tf?
5. Why define versions?
6. What makes a good Terraform module?
7. Why avoid large modules?
8. How do teams standardize modules?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- main.tf contains infrastructure logic.
- variables.tf defines inputs.
- outputs.tf exports values.
- versions.tf manages compatibility.
- Good modules are reusable and focused.
- Core Terraform module-design topic.