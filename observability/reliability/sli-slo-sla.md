

# SLI, SLO and SLA

## Overview

SLI, SLO, and SLA are core reliability engineering concepts used to measure, manage, and communicate service reliability.

They help engineering teams define service quality expectations, monitor performance, and balance reliability with feature delivery.

These concepts are foundational in Site Reliability Engineering (SRE) and modern platform operations.

---

## Why SLI, SLO and SLA Matter

Without Reliability Targets:

```text
Service Quality
       ↓
Unclear Expectations
       ↓
Operational Risk
```

With Reliability Targets:

```text
Service Quality
       ↓
SLI
       ↓
SLO
       ↓
SLA
       ↓
Clear Expectations
```

Benefits:

- Measurable Reliability
- Better User Experience
- Improved Service Quality
- Clear Operational Goals
- Better Business Alignment

---

## SLI (Service Level Indicator)

An SLI is a measurable indicator of service performance.

Examples:

- Request Success Rate
- Service Availability
- Response Time
- Error Rate

Example:

```text
Successful Requests
------------------- = 99.95%
Total Requests
```

SLIs answer:

```text
How is the service performing?
```

---

## SLO (Service Level Objective)

An SLO is a reliability target based on an SLI.

Examples:

```text
Availability >= 99.9%
Latency < 200ms
```

SLOs answer:

```text
What reliability target should be achieved?
```

---

## SLA (Service Level Agreement)

An SLA is a formal agreement defining expected service levels.

Examples:

```text
99.9% Monthly Availability
```

May include:

- Business Commitments
- Service Expectations
- Financial Penalties
- Support Requirements

SLAs answer:

```text
What was promised to customers?
```

---

## Relationship Between SLI, SLO and SLA

```text
SLI
 ↓
Measurement
 ↓
SLO
 ↓
Target
 ↓
SLA
 ↓
Customer Commitment
```

---

## Error Budget

Error Budget represents the acceptable amount of unreliability.

Example:

```text
SLO = 99.9%

Allowed Failure = 0.1%
```

Benefits:

- Balances Reliability And Innovation
- Prevents Excessive Risk
- Supports Engineering Decisions

---

## Common Production Usage

Used for:

- Site Reliability Engineering
- Cloud Platforms
- Kubernetes Operations
- Service Management
- Incident Management
- Reliability Reporting

---

## SLI vs SLO vs SLA

| Concept | Purpose | Audience |
|----------|----------|----------|
| SLI | Measurement | Engineering Teams |
| SLO | Reliability Target | Engineering Teams |
| SLA | Customer Commitment | Customers And Business |

---

## Production Engineering Perspective

### Common Challenges

- Poor SLI Selection
- Unrealistic SLO Targets
- Missing Error Budgets
- Misaligned Business Expectations
- Reliability Measurement Gaps

---

## Most Asked Questions

1. What is an SLI?
2. What is an SLO?
3. What is an SLA?
4. SLI vs SLO vs SLA?
5. What is an Error Budget?
6. Why are SLOs important?
7. How do teams define reliability targets?
8. How are these concepts used in SRE?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- SLI measures service performance.
- SLO defines a reliability target.
- SLA defines a customer commitment.
- Error Budgets balance reliability and innovation.
- Core SRE concepts.
- Frequently asked in interviews.