

# CloudTrail

## Overview

AWS CloudTrail is a monitoring and auditing service that records AWS account activity and API operations.

It helps organizations track who performed an action, when it occurred, and which AWS resources were affected.

CloudTrail is a core service for security, governance, compliance, and operational auditing.

---

## Why CloudTrail Matters

Without CloudTrail:

```text
AWS Changes
      ↓
No Audit History
      ↓
Limited Visibility
```

With CloudTrail:

```text
AWS Changes
      ↓
CloudTrail Logs
      ↓
Full Audit History
```

Benefits:

- Security Monitoring
- Auditability
- Compliance Support
- Operational Visibility
- Incident Investigation

---

## How CloudTrail Works

```text
User / Service
        ↓
AWS API Call
        ↓
CloudTrail Event
        ↓
Audit Logs
```

CloudTrail records activities performed across AWS services.

---

## What CloudTrail Records

Examples:

- IAM Changes
- EC2 Operations
- S3 Activity
- Security Group Changes
- Resource Creation
- Resource Deletion

---

## Event Components

CloudTrail events typically contain:

- User Identity
- Event Time
- AWS Service
- API Action
- Source IP Address
- Request Details

---

## Common Use Cases

### Security Auditing

Examples:

- Permission Changes
- Unauthorized Access Attempts
- Resource Modifications

---

### Compliance

Examples:

- Audit Requirements
- Regulatory Reporting
- Governance Reviews

---

### Troubleshooting

Examples:

- Who Deleted A Resource?
- Who Modified Security Settings?
- When Did A Change Occur?

---

## Common Production Architecture

```text
AWS Services
       ↓
CloudTrail
       ↓
Audit Logs
       ↓
Security Team
```

---

## Real Production Example

```text
Engineer
    ↓
Deletes EC2 Instance
    ↓
CloudTrail Records Event
    ↓
Audit Investigation
```

Benefits:

- Accountability
- Traceability
- Security Visibility

---

## CloudTrail vs CloudWatch

| Feature | CloudTrail | CloudWatch |
|----------|-----------|------------|
| Primary Purpose | Auditing | Monitoring |
| Tracks API Calls | Yes | No |
| Security Investigation | Yes | Limited |
| Performance Metrics | No | Yes |
| Operational Monitoring | Limited | Yes |

---

## Production Engineering Perspective

### Common Challenges

- Missing Audit Reviews
- Log Retention Issues
- Excessive Event Volume
- Compliance Requirements
- Security Investigations

---

## Most Asked Questions

1. What is AWS CloudTrail?
2. What does CloudTrail record?
3. Why is CloudTrail important?
4. CloudTrail vs CloudWatch?
5. How does CloudTrail help security teams?
6. Can CloudTrail identify who made a change?
7. What information is stored in events?
8. How is CloudTrail used for compliance?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- CloudTrail records AWS API activity.
- Used for auditing and compliance.
- Helps identify who performed an action.
- Critical for security investigations.
- Complements CloudWatch monitoring.
- Core AWS governance service.