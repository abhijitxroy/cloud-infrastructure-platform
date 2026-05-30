

# Terraform Apply

## Overview

Terraform Apply is the command used to create, update, or modify infrastructure based on the Terraform execution plan.

It is the stage where infrastructure changes are actually performed.

Terraform Apply takes the desired infrastructure configuration and makes changes to the target environment to match that configuration.

---

## Why Terraform Apply Matters

Without Apply:

```text
Terraform Configuration
          ↓
Terraform Plan
          ↓
No Infrastructure Changes
```

With Apply:

```text
Terraform Configuration
          ↓
Terraform Plan
          ↓
Terraform Apply
          ↓
Infrastructure Updated
```

Benefits:

- Infrastructure Automation
- Consistent Deployments
- Reduced Manual Work
- Repeatable Operations

---

## Apply Workflow

```text
Terraform Configuration
          ↓
Terraform Plan
          ↓
Terraform Apply
          ↓
Infrastructure Changes
```

Terraform compares:

```text
Desired State
      vs
Current State
```

to determine required changes.

---

## Common Apply Actions

### Resource Creation

Examples:

- VPC Creation
- Virtual Machine Provisioning
- Database Deployment

---

### Resource Updates

Examples:

- Configuration Changes
- Scaling Changes
- Security Updates

---

### Resource Replacement

Some infrastructure changes require:

```text
Destroy Resource
       ↓
Create New Resource
```

Replacement may impact availability.

---

### No Changes

If infrastructure already matches the desired state:

```text
No Changes Required
```

---

## Why Review Plans Before Apply

Always review:

```text
terraform plan
```

before:

```text
terraform apply
```

Benefits:

- Prevents Mistakes
- Detects Unexpected Changes
- Reduces Production Risk

---

## Production Deployment Flow

```text
Code Change
      ↓
Validation
      ↓
Terraform Plan
      ↓
Review
      ↓
Approval
      ↓
Terraform Apply
      ↓
Infrastructure Updated
```

---

## Common Risks

### Applying Unreviewed Changes

Can result in:

- Service Disruption
- Resource Deletion
- Misconfiguration

---

### Unexpected Resource Replacement

Can cause:

- Downtime
- Infrastructure Changes
- Operational Impact

---

### Permission Issues

May prevent infrastructure deployment.

---

## Real Production Example

```text
Git Commit
     ↓
Pull Request
     ↓
Terraform Plan
     ↓
Approval
     ↓
Terraform Apply
     ↓
AWS Infrastructure
```

Benefits:

- Controlled Changes
- Better Governance
- Reliable Deployments

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Failed Apply Operations
- Permission Problems
- State Conflicts
- Dependency Issues
- Resource Replacement Risks

---

## Most Asked Questions

1. What is Terraform Apply?
2. What happens during Terraform Apply?
3. Why review plans before Apply?
4. Can Terraform Apply create resources?
5. Can Terraform Apply update resources?
6. When are resources replaced?
7. What are common Apply risks?
8. How do teams safely run Terraform Apply?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Terraform Apply executes infrastructure changes.
- Apply follows Terraform Plan.
- Always review plans before applying.
- Apply can create, update, or replace resources.
- Production deployments typically require approvals.
- Core Terraform workflow topic.