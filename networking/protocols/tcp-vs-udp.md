# TCP vs UDP

## Overview

TCP and UDP are transport layer communication protocols commonly used in networking environments.

They provide different approaches for transferring information between systems based on application requirements.

Protocol selection influences reliability, latency and communication behavior.

---

## TCP

Transmission Control Protocol (TCP) focuses on reliable communication.

Characteristics:

- Connection oriented communication
- Ordered data delivery
- Error checking
- Packet retransmission support
- Higher reliability

Common examples:

- HTTP
- HTTPS
- SSH
- Database communication

TCP is commonly used where delivery accuracy is important.

---

## UDP

User Datagram Protocol (UDP) focuses on lightweight communication with lower overhead.

Characteristics:

- Connectionless communication
- Lower latency
- No delivery guarantee
- Reduced communication overhead

Common examples:

- DNS
- Video streaming
- Voice communication
- Real time applications

UDP is commonly used where speed becomes more important than guaranteed delivery.

---

## Communication Model

TCP:

Sender

↓

Connection Establishment

↓

Reliable Data Transfer

↓

Acknowledgement

UDP:

Sender

↓

Data Transmission

↓

Receiver

---

## Operational Considerations

Protocol selection commonly depends on:

- Reliability requirements
- Performance requirements
- Application communication pattern
- Latency expectations

---

## Notes

Transport protocols influence application behavior and infrastructure communication patterns across distributed environments.