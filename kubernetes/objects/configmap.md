

# ConfigMap

## Overview

A ConfigMap is a Kubernetes object used to store non-sensitive configuration data.

Applications can read configuration values from ConfigMaps instead of hardcoding them inside container images.

Examples:

- Application Settings
- Environment Variables
- Configuration Files
- Feature Flags

ConfigMaps help separate configuration from application code.

---

## Why ConfigMaps Matter

Without ConfigMaps:

```text
Configuration
      ↓
Embedded In Image
      ↓
Image Rebuild Required
```

With ConfigMaps:

```text
Configuration
      ↓
ConfigMap
      ↓
Application
```

Benefits:

- Easier Configuration Management
- Environment Separation
- Reduced Image Rebuilds
- Better Operational Flexibility

---

## Architecture

```text
ConfigMap
      ↓
Deployment
      ↓
Pod
      ↓
Application
```

---

## Common Use Cases

### Application Configuration

Examples:

```text
application.name
application.mode
application.region
```

---

### Environment Variables

Examples:

```text
LOG_LEVEL=INFO
APP_MODE=PROD
```

---

### Configuration Files

Examples:

```text
application.properties
nginx.conf
```

---

## How Applications Consume ConfigMaps

### Environment Variables

```text
ConfigMap
      ↓
Environment Variables
      ↓
Application
```

---

### Mounted Files

```text
ConfigMap
      ↓
Volume Mount
      ↓
Configuration File
```

---

## ConfigMap vs Secret

| ConfigMap | Secret |
| ---------- | ------ |
| Non-Sensitive Data | Sensitive Data |
| Plain Configuration | Credentials |
| Feature Flags | Passwords |
| Application Settings | API Keys |

---

## Real Production Example

```text
Spring Boot Application
          ↓
ConfigMap
          ↓
LOG_LEVEL
DATABASE_HOST
FEATURE_FLAGS
```

Benefits:

- Environment Specific Configuration
- Easier Updates
- Cleaner Deployments

---

## Production Engineering Perspective

### Common Troubleshooting Areas

- Missing Configuration
- Incorrect Environment Variables
- Mount Failures
- Configuration Drift
- Application Startup Errors

---

## Most Asked Interview Questions

1. What is a ConfigMap?
2. Why are ConfigMaps needed?
3. What data should be stored in a ConfigMap?
4. How is a ConfigMap consumed by Pods?
5. ConfigMap vs Secret?
6. Can ConfigMaps store files?
7. Why separate configuration from code?
8. What happens if a ConfigMap is missing?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- ConfigMaps store non-sensitive configuration.
- ConfigMaps separate configuration from application code.
- Applications consume ConfigMaps through environment variables or mounted files.
- ConfigMaps improve deployment flexibility.
- Secrets should be used for sensitive data.
- Frequently asked Kubernetes interview topic.