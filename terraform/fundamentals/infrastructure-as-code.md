

# Infrastructure as Code (IaC)

## Overview

Infrastructure as Code (IaC) is the practice of managing and provisioning infrastructure through code instead of manual processes.

Using IaC, engineers define infrastructure in version-controlled files that can be reviewed, tested, deployed, and maintained like application code.

Terraform is one of the most widely used Infrastructure as Code platforms.

---

## Why Infrastructure as Code Matters

Without IaC:

```text
Manual Changes
       ↓
Inconsistent Environments
       ↓
Operational Problems
```

With IaC:

```text
Infrastructure Code
         ↓
Version Control
         ↓
Automated Provisioning
         ↓
Consistent Infrastructure
```

Benefits:

- Automation
- Consistency
- Repeatability
- Auditability
- Faster Deployments

---

## Traditional Infrastructure vs IaC

| Traditional Infrastructure | Infrastructure as Code |
| -------------------------- | ---------------------- |
| Manual Configuration | Automated Provisioning |
| Error Prone | Repeatable |
| Difficult Auditing | Version Controlled |
| Slow Changes | Faster Changes |

---

## How IaC Works

```text
Infrastructure Code
         ↓
Terraform
         ↓
Cloud Provider APIs
         ↓
Infrastructure Created
```

Engineers describe the desired infrastructure state and Terraform provisions the required resources.

---

## Core Principles

### Version Control

Infrastructure definitions should be stored in Git repositories.

Benefits:

- Change Tracking
- Collaboration
- Rollback Capability

---

### Automation

Infrastructure creation should be automated.

Examples:

- Servers
- Networks
- Databases
- Kubernetes Clusters

---

### Consistency

The same code should produce the same infrastructure repeatedly.

---

### Idempotency

Repeated executions should produce the same desired state.

---

## Common IaC Tools

### Terraform

Multi-cloud infrastructure provisioning.

---

### AWS CloudFormation

AWS-native infrastructure automation.

---

### Pulumi

Infrastructure defined using programming languages.

---

### Ansible

Configuration management and automation.

---

## Real Production Example

```text
Terraform Code
       ↓
AWS VPC
       ↓
Subnets
       ↓
Load Balancer
       ↓
EKS Cluster
```

Benefits:

- Standardized Deployments
- Faster Provisioning
- Reduced Human Error

---

## Production Engineering Perspective

### Common Challenges

- Infrastructure Drift
- State Management
- Environment Separation
- Access Control
- Change Governance

---

## Most Asked Interview Questions

1. What is Infrastructure as Code?
2. Why is IaC important?
3. Traditional Infrastructure vs IaC?
4. What are the benefits of IaC?
5. What is idempotency?
6. Why store infrastructure in Git?
7. What tools support IaC?
8. How does Terraform implement IaC?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- IaC manages infrastructure through code.
- Infrastructure becomes version controlled.
- Automation improves consistency.
- Terraform is a popular IaC platform.
- IaC reduces manual errors.
- Foundational Terraform and platform engineering concept.