# DNS Overview

## Overview

Domain Name System (DNS) provides a mechanism for translating human readable names into IP addresses.

Applications and infrastructure systems commonly rely on DNS to locate services and establish communication across environments.

DNS helps reduce dependency on manually managing infrastructure addresses.

---

## Common Responsibilities

DNS commonly supports:

- Name resolution
- Service discovery
- Traffic routing support
- Infrastructure abstraction

---

## Resolution Flow

Example workflow:

Application Request

↓

DNS Query

↓

DNS Resolver

↓

DNS Server

↓

IP Address Response

↓

Target System Communication

DNS enables systems to communicate without directly depending on infrastructure addressing details.

---

## Common Record Types

Examples:

### A Record

Maps domain name to IPv4 address.

### AAAA Record

Maps domain name to IPv6 address.

### CNAME

Creates alias mapping.

### MX Record

Mail routing configuration.

### TXT Record

Additional metadata or validation information.

---

## Operational Benefits

DNS helps improve:

- Infrastructure flexibility
- Service discovery
- Operational maintainability
- Application portability

---

## Notes

DNS becomes increasingly important as infrastructure environments expand across cloud systems, distributed services and container platforms.