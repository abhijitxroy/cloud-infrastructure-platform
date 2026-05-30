

# Terraform vs CloudFormation

## Overview

Terraform and CloudFormation are Infrastructure as Code (IaC) platforms used to provision and manage infrastructure through code.

Both automate infrastructure deployment, but they differ in ecosystem support, portability, and operational flexibility.

---

## Why This Comparison Matters

Organizations often need to choose between:

```text
Terraform
or
CloudFormation
```

The choice impacts:

- Portability
- Vendor Lock-In
- Team Operations
- Infrastructure Governance

---

## High-Level Comparison

| Terraform | CloudFormation |
| ---------- | -------------- |
| Multi-Cloud | AWS Only |
| Open Source | AWS Managed |
| Provider Ecosystem | AWS Ecosystem |
| Platform Independent | AWS Specific |
| Large Community | AWS Native Integration |

---

## Infrastructure Support

### Terraform

Supports:

- AWS
- Azure
- Google Cloud
- Kubernetes
- GitHub
- Datadog
- Hundreds of Providers

---

### CloudFormation

Supports:

- AWS Services
- AWS Resources

Best suited for AWS-only environments.

---

## Architecture

### Terraform

```text
Terraform
      ↓
Provider
      ↓
Cloud APIs
```

---

### CloudFormation

```text
CloudFormation
       ↓
AWS APIs
       ↓
AWS Resources
```

---

## State Management

### Terraform

Uses:

```text
terraform.tfstate
```

Tracks infrastructure state explicitly.

---

### CloudFormation

AWS manages stack state automatically.

No separate state file is required.

---

## Multi-Cloud Support

### Terraform

Strong multi-cloud capabilities.

Example:

```text
AWS
Azure
Google Cloud
```

managed from a single platform.

---

### CloudFormation

Limited to AWS resources.

---

## Reusability

### Terraform

Uses:

```text
Modules
```

for reusable infrastructure.

---

### CloudFormation

Uses:

```text
Nested Stacks
```

for reuse.

---

## Common Use Cases

### Terraform

- Multi-Cloud Infrastructure
- Kubernetes Platforms
- Platform Engineering
- Hybrid Cloud Environments

---

### CloudFormation

- AWS-Centric Organizations
- Native AWS Automation
- AWS Governance Requirements

---

## Real Production Example

### Terraform

```text
AWS Infrastructure
      ↓
Kubernetes Cluster
      ↓
Datadog Monitoring
```

Single workflow across platforms.

---

### CloudFormation

```text
AWS VPC
     ↓
AWS Load Balancer
     ↓
AWS ECS
```

Optimized for AWS environments.

---

## Production Engineering Perspective

### Choose Terraform When

- Multi-Cloud Support Is Needed
- Kubernetes Is A Major Platform
- Reusable Modules Are Important
- Platform Standardization Is Required

---

### Choose CloudFormation When

- AWS Is The Only Cloud
- Native AWS Integration Is Preferred
- AWS Governance Is A Priority

---

## Most Asked Interview Questions

1. Terraform vs CloudFormation?
2. Which supports multi-cloud deployments?
3. How does Terraform manage state?
4. What are Terraform modules?
5. What are CloudFormation stacks?
6. When should CloudFormation be preferred?
7. Why is Terraform popular for platform engineering?
8. What are the tradeoffs between the two?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Terraform is multi-cloud.
- CloudFormation is AWS-specific.
- Terraform uses providers and state files.
- CloudFormation manages state internally.
- Terraform modules improve reusability.
- One of the most common IaC comparison topics.