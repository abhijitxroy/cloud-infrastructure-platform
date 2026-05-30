

# Terraform Plan

## Overview

Terraform Plan is the command used to preview infrastructure changes before they are applied.

It compares the desired infrastructure configuration with the current infrastructure state and generates an execution plan showing what Terraform intends to do.

Terraform Plan is one of the most important safety mechanisms in Terraform workflows.

---

## Why Terraform Plan Matters

Without Plan:

```text
Configuration Change
          ↓
Immediate Deployment
          ↓
Operational Risk
```

With Plan:

```text
Configuration Change
          ↓
Terraform Plan
          ↓
Review Changes
          ↓
Safe Deployment
```

Benefits:

- Change Visibility
- Risk Reduction
- Safer Deployments
- Better Governance

---

## How Terraform Plan Works

```text
Terraform Configuration
          ↓
Terraform State
          ↓
Current Infrastructure
          ↓
Terraform Plan
```

Terraform compares:

```text
Desired State
      vs
Current State
```

and identifies required actions.

---

## Common Plan Results

### Resource Creation

Examples:

- New VPC
- New Database
- New Kubernetes Cluster

---

### Resource Updates

Examples:

- Configuration Changes
- Scaling Adjustments
- Security Updates

---

### Resource Replacement

Some modifications require:

```text
Destroy Resource
       ↓
Create New Resource
```

This should be reviewed carefully.

---

### Resource Deletion

Terraform may identify resources that will be removed.

---

## Why Review Plans

Plans help identify:

- Unexpected Changes
- Accidental Deletions
- Resource Replacements
- Configuration Errors

Reviewing plans reduces deployment risk.

---

## Production Workflow

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
```

---

## Common Risks

### Ignoring Plan Output

Can result in:

- Service Disruption
- Resource Deletion
- Unexpected Infrastructure Changes

---

### Unreviewed Replacements

May cause:

- Downtime
- Operational Impact

---

### Infrastructure Drift

Plans may reveal differences between configuration and actual infrastructure.

---

## Real Production Example

```text
Pull Request
      ↓
Terraform Plan
      ↓
Team Review
      ↓
Approval
      ↓
Terraform Apply
```

Benefits:

- Better Visibility
- Safer Deployments
- Improved Governance

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Unexpected Resource Changes
- State Issues
- Dependency Problems
- Drift Detection
- Configuration Errors

---

## Most Asked Questions

1. What is Terraform Plan?
2. Why is Terraform Plan important?
3. What does Terraform Plan compare?
4. Why review plans before Apply?
5. What information does a Plan provide?
6. How can Plan reduce deployment risk?
7. What is infrastructure drift?
8. How do teams use Terraform Plan in production?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- Terraform Plan previews infrastructure changes.
- Plan compares desired and current state.
- Always review plans before Apply.
- Plan identifies creates, updates, replacements, and deletions.
- Core Terraform safety mechanism.
- Essential production workflow practice.