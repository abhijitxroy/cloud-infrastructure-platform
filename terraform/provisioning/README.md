

# Provisioning

## Overview

Provisioning focuses on how Terraform creates, initializes, and prepares infrastructure resources for use.

It covers techniques used during resource creation, initialization, validation, and post-deployment automation.

Provisioning is an important part of infrastructure automation but should remain focused on infrastructure lifecycle activities rather than long-term configuration management.

---

## Why Provisioning Matters

Without Provisioning:

```text
Infrastructure Created
         ↓
Manual Setup
         ↓
Operational Overhead
```

With Provisioning:

```text
Infrastructure Created
         ↓
Automated Initialization
         ↓
Ready For Use
```

Benefits:

- Faster Deployments
- Reduced Manual Work
- Consistent Setup
- Improved Automation

---

## Topics Covered

### Provisioners

Focus Areas:

- Local Provisioners
- Remote Provisioners
- Initialization Tasks
- Validation Tasks
- Automation Workflows

---

## Common Provisioning Activities

### Infrastructure Initialization

Examples:

- Server Bootstrap
- Agent Installation
- Runtime Preparation

---

### Validation

Examples:

- Connectivity Checks
- Health Verification
- Deployment Validation

---

### Integration

Examples:

- External Automation
- Monitoring Registration
- Service Registration

---

## Learning Path

```text
Infrastructure Creation
         ↓
Provisioners
         ↓
Initialization Tasks
         ↓
Validation
         ↓
Production Automation
```

---

## Real Production Usage

Provisioning is commonly used for:

- Server Initialization
- Monitoring Agent Installation
- Bootstrap Automation
- Environment Preparation
- Deployment Validation

---

## Production Engineering Perspective

### Common Risks

- Script Failures
- Configuration Drift
- Long Deployments
- Non-Repeatable Processes
- Environment Inconsistencies

---

## Most Asked Interview Questions

1. What is Terraform Provisioning?
2. What are Provisioners?
3. Local vs Remote Provisioners?
4. When should Provisioners be used?
5. Why are Provisioners often discouraged?
6. What are common Provisioning use cases?
7. What alternatives exist to Provisioners?
8. What are Provisioning best practices?

---

## Quick Revision

### Priority

⭐⭐⭐ Medium Priority

### Remember

- Provisioning prepares infrastructure for use.
- Provisioners automate initialization tasks.
- Use Provisioners sparingly.
- Prefer dedicated configuration management tools for ongoing configuration.
- Keep provisioning workflows simple and repeatable.
- Terraform is primarily an infrastructure provisioning platform.