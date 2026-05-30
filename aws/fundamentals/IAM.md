#IAM

<img width="1545" alt="image" src="https://github.com/abhijitxroy/aws/assets/161963891/ca00ce93-8530-45f8-a0ff-c5a43acb2e31">

<img width="1486" alt="image" src="https://github.com/abhijitxroy/aws/assets/161963891/57e6d6ef-35ab-4f8d-9945-bc4766a3dc46">

IAM - Global Service there is no region to be selected
-

<img width="1486" alt="image" src="https://github.com/abhijitxroy/aws/assets/161963891/d6a52fa2-295f-43aa-9308-902a63f1452f">

<img width="1573" alt="image" src="https://github.com/abhijitxroy/aws/assets/161963891/b69c0576-b688-4136-b87c-fed364a225f7">

<img width="1573" alt="image" src="https://github.com/abhijitxroy/aws/assets/161963891/0f51812d-e25a-40a4-b1d9-dc9cf75b7ae7">

<img width="1573" alt="image" src="https://github.com/abhijitxroy/aws/assets/161963891/71d54091-5e69-4061-ab5b-ae0a076b86d0">

<img width="1573" alt="image" src="https://github.com/abhijitxroy/aws/assets/161963891/1333b4a1-ae74-4207-89d4-ceda38e03b20">

<img width="1573" alt="image" src="https://github.com/abhijitxroy/aws/assets/161963891/1d43e690-aeb0-46ca-a523-3b972a2d2f46">

<img width="1573" alt="image" src="https://github.com/abhijitxroy/aws/assets/161963891/15b43b8e-7e32-403b-950f-9bf4cff48e71">

<img width="897" alt="image" src="https://github.com/abhijitxroy/aws/assets/161963891/01c32aff-e34f-41bd-aa0a-64ce487cfb2c">

<img width="761" alt="image" src="https://github.com/abhijitxroy/aws/assets/161963891/8c1e022f-6636-4ab6-96c6-12d8fea7fa31">

<img width="1508" alt="image" src="https://github.com/abhijitxroy/aws/assets/161963891/26009ccf-c6e6-4d25-8e66-03c45b8861e2">

<img width="1508" alt="image" src="https://github.com/abhijitxroy/aws/assets/161963891/47ac64c1-fba4-4d28-ad0d-f9dadaa3ea56">

<img width="1508" alt="image" src="https://github.com/abhijitxroy/aws/assets/161963891/663a4cd6-9e92-4d9f-b4db-48aefff201bb">

# IAM

## Overview

AWS Identity and Access Management (IAM) is the service used to control authentication and authorization within AWS.

IAM enables organizations to securely manage users, groups, roles, and permissions for AWS resources.

IAM is one of the most important AWS services because every AWS environment depends on access control.

---

## Why IAM Matters

Without IAM:

```text
Users
  ↓
Unlimited Access
  ↓
Security Risks
```

With IAM:

```text
Users
  ↓
IAM Policies
  ↓
Controlled Access
```

Benefits:

- Access Control
- Security Enforcement
- Least Privilege Access
- Governance
- Compliance

---

## IAM Is A Global Service

IAM operates globally within an AWS Account.

```text
AWS Account
      ↓
IAM
      ↓
All AWS Regions
```

IAM resources are not tied to a specific AWS Region.

---

## Core Components

### IAM Users

IAM Users represent individual identities.

Examples:

- Engineers
- Administrators
- Developers
- Support Teams

---

### IAM Groups

Groups are collections of users.

Example:

```text
Developers Group
      ↓
Multiple Developers
```

Benefits:

- Easier Permission Management
- Simplified Administration

---

### IAM Roles

Roles provide temporary permissions.

Common Uses:

- EC2 Access
- Lambda Access
- Cross-Account Access
- Application Access

---

### IAM Policies

Policies define permissions.

Examples:

- Allow S3 Access
- Allow EC2 Access
- Deny Specific Actions

---

## Authentication vs Authorization

### Authentication

Verifies identity.

Example:

```text
Who Are You?
```

---

### Authorization

Determines permissions.

Example:

```text
What Can You Do?
```

---

## Principle Of Least Privilege

Users should receive only the permissions required to perform their tasks.

```text
Minimum Permissions
        ↓
Reduced Security Risk
```

This is a core IAM best practice.

---

## Common Production Architecture

```text
User
 ↓
IAM User / Role
 ↓
IAM Policy
 ↓
AWS Resource
```

---

## Security Best Practices

- Enable MFA
- Follow Least Privilege
- Avoid Root User Usage
- Use Roles Instead Of Long-Term Credentials
- Regularly Review Permissions

---

## Real Production Example

```text
Developer
      ↓
IAM Group
      ↓
Read-Only Access
      ↓
AWS Resources
```

Benefits:

- Controlled Access
- Better Security
- Easier Governance

---

## Production Engineering Perspective

### Common Challenges

- Excessive Permissions
- Unused Users
- Missing MFA
- Shared Credentials
- Poor Permission Design

---

## Most Asked Questions

1. What is IAM?
2. Why is IAM important?
3. What is the difference between Users, Groups, and Roles?
4. What are IAM Policies?
5. What is Least Privilege?
6. Why is IAM a global service?
7. Why use Roles instead of users for applications?
8. What are IAM security best practices?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- IAM controls authentication and authorization.
- IAM is a global AWS service.
- Users represent identities.
- Groups simplify permission management.
- Roles provide temporary access.
- Policies define permissions.
- Least Privilege is a core security principle.