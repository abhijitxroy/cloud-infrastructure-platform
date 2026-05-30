

# Variables and Outputs

## Overview

Variables and Outputs enable Terraform configurations to become reusable, flexible, and maintainable.

Variables allow infrastructure configurations to accept input values, while Outputs expose useful information from deployed infrastructure.

Together they improve module design, environment management, and infrastructure reuse.

---

## Why Variables and Outputs Matter

Without Variables:

```text
Hardcoded Configuration
         ↓
Limited Reusability
```

With Variables:

```text
Configurable Infrastructure
           ↓
Reusable Deployments
```

Without Outputs:

```text
Infrastructure Created
         ↓
No Shared Information
```

With Outputs:

```text
Infrastructure Created
         ↓
Useful Information Shared
```

Benefits:

- Reusability
- Flexibility
- Maintainability
- Environment Standardization

---

## Variables

Variables provide input values to Terraform configurations.

Examples:

- Environment Name
- Region
- Instance Type
- Network Range

---

## Why Variables Are Important

Without Variables:

```text
Development Configuration
       ↓
Copied For Production
```

With Variables:

```text
Reusable Configuration
        ↓
Development
Staging
Production
```

---

## Common Variable Usage

### Environment Configuration

Examples:

- Development
- Staging
- Production

---

### Resource Sizing

Examples:

- Instance Types
- Storage Sizes
- Node Counts

---

### Regional Deployments

Examples:

- AWS Regions
- Multi-Region Infrastructure

---

## Outputs

Outputs expose information from deployed infrastructure.

Examples:

- VPC IDs
- Load Balancer Endpoints
- Database Endpoints
- Kubernetes Cluster Information

---

## Why Outputs Are Important

Outputs allow:

```text
Module A
   ↓
Output Value
   ↓
Module B
```

This enables infrastructure components to work together.

---

## Common Output Examples

### Networking

- VPC ID
- Subnet IDs

---

### Compute

- Instance IDs
- Public IP Addresses

---

### Platform Services

- Cluster Endpoints
- Service URLs

---

## Variables and Outputs Together

```text
Input Variables
        ↓
Terraform Resources
        ↓
Output Values
```

This creates reusable infrastructure building blocks.

---

## Real Production Example

```text
Networking Module
        ↓
Outputs VPC ID
        ↓
Kubernetes Module
        ↓
Uses VPC ID
```

Benefits:

- Loose Coupling
- Better Reusability
- Standardized Infrastructure

---

## Production Engineering Perspective

### Common Challenges

- Hardcoded Values
- Missing Outputs
- Variable Sprawl
- Environment Inconsistency
- Poor Module Design

---

## Most Asked Interview Questions

1. What are Terraform Variables?
2. Why are Variables important?
3. What are Terraform Outputs?
4. Why are Outputs needed?
5. How do Modules use Outputs?
6. How do Variables improve reusability?
7. What are common Variable design mistakes?
8. How do Outputs enable module communication?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Variables provide input values.
- Outputs expose infrastructure information.
- Variables improve flexibility.
- Outputs enable module communication.
- Together they improve reusability.
- Core Terraform module and resource-management concept.