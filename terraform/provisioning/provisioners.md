

# Provisioners

## Overview

Provisioners are Terraform components used to execute scripts or commands on local systems or provisioned resources.

They are typically used for bootstrapping, configuration tasks, or post-deployment actions.

Provisioners should be used carefully because they introduce operational complexity and can reduce infrastructure predictability.

---

## Why Provisioners Matter

Provisioners can help automate tasks that occur after infrastructure creation.

Examples:

- Software Installation
- Configuration Updates
- Initialization Scripts
- Validation Tasks

---

## How Provisioners Work

```text
Terraform Resource
         ↓
Provisioner
         ↓
Command Execution
         ↓
Configuration Complete
```

Provisioners run after resource creation or before resource destruction depending on configuration.

---

## Common Provisioner Types

### Local Provisioner

Runs commands on the machine executing Terraform.

Typical Uses:

- Generate Files
- Trigger Scripts
- Notify External Systems

---

### Remote Provisioner

Runs commands on the created infrastructure resource.

Typical Uses:

- Install Packages
- Configure Applications
- Initialize Servers

---

## Typical Use Cases

### Server Initialization

Examples:

- Install Web Servers
- Configure Runtime Dependencies
- Setup Monitoring Agents

---

### Validation Tasks

Examples:

- Connectivity Checks
- Health Verification
- Deployment Validation

---

### Integration Tasks

Examples:

- Trigger Automation
- Register Services
- Update Inventory Systems

---

## Why Provisioners Are Often Avoided

Terraform focuses on:

```text
Infrastructure Provisioning
```

not:

```text
Configuration Management
```

Many teams prefer:

- Ansible
- Chef
- Puppet
- Cloud-Init
- Kubernetes Operators

for configuration management activities.

---

## Best Practices

### Use Provisioners Sparingly

Prefer native platform capabilities whenever possible.

---

### Keep Tasks Simple

Avoid complex business logic.

---

### Prefer Immutable Infrastructure

Provision infrastructure once and replace rather than modifying repeatedly.

---

### Separate Configuration Management

Use dedicated tools for ongoing server configuration.

---

## Real Production Example

```text
EC2 Instance
      ↓
Provisioner
      ↓
Install Monitoring Agent
      ↓
Register With Monitoring Platform
```

---

## Production Engineering Perspective

### Common Challenges

- Script Failures
- Connectivity Problems
- Long Deployment Times
- Non-Repeatable Behavior
- Configuration Drift

---

## Most Asked Interview Questions

1. What are Terraform Provisioners?
2. When should Provisioners be used?
3. Local vs Remote Provisioners?
4. Why are Provisioners discouraged in some environments?
5. What alternatives exist to Provisioners?
6. What are common Provisioner use cases?
7. How do Provisioners affect reliability?
8. What are Provisioner best practices?

---

## Quick Revision

### Priority

⭐⭐⭐ Medium Priority

### Remember

- Provisioners execute commands after resource creation.
- Local Provisioners run on the Terraform host.
- Remote Provisioners run on target resources.
- Use Provisioners sparingly.
- Prefer dedicated configuration management tools.
- Terraform is primarily an infrastructure provisioning tool.