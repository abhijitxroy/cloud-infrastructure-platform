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
# TCP vs UDP

## Overview

TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are the two primary transport layer protocols used for communication across networks.

Both protocols transfer data between systems, but they differ significantly in reliability, speed, connection management, and use cases.

Understanding TCP and UDP is essential for cloud networking, Kubernetes networking, distributed systems, platform engineering, and production troubleshooting.

---

## Why TCP And UDP Matter

Different applications have different communication requirements.

Examples:

```text
Banking Transaction
        ↓
Reliable Delivery Required
        ↓
TCP
```

```text
Video Streaming
        ↓
Low Latency Required
        ↓
UDP
```

Benefits:

- Efficient Communication
- Application Optimization
- Better Performance
- Reliable Data Transfer
- Reduced Network Overhead

---

## TCP (Transmission Control Protocol)

TCP focuses on reliable communication.

Characteristics:

- Connection-Oriented Communication
- Ordered Data Delivery
- Error Detection
- Packet Retransmission
- Reliable Delivery

---

### How TCP Works

```text
Client
   ↓
Connection Establishment
   ↓
Reliable Data Transfer
   ↓
Acknowledgement
   ↓
Connection Termination
```

---

### Common TCP Use Cases

Examples:

- HTTP
- HTTPS
- SSH
- Database Communication
- File Transfers
- Email Services

TCP is used when delivery accuracy is more important than speed.

---

## UDP (User Datagram Protocol)

UDP focuses on lightweight communication with minimal overhead.

Characteristics:

- Connectionless Communication
- Lower Latency
- No Delivery Guarantee
- No Retransmission
- Reduced Overhead

---

### How UDP Works

```text
Sender
   ↓
Data Transmission
   ↓
Receiver
```

UDP sends data without establishing a connection.

---

### Common UDP Use Cases

Examples:

- DNS
- Video Streaming
- Voice Communication
- Online Gaming
- Real-Time Applications
- Media Broadcasting

UDP is used when speed is more important than guaranteed delivery.

---

## TCP vs UDP Comparison

| Feature | TCP | UDP |
|----------|-----|-----|
| Connection | Connection-Oriented | Connectionless |
| Reliability | High | Low |
| Packet Ordering | Guaranteed | Not Guaranteed |
| Retransmission | Supported | Not Supported |
| Speed | Slower | Faster |
| Overhead | Higher | Lower |
| Common Use Cases | Web, Databases, SSH | Streaming, DNS, Gaming |

---

## Production Usage

### TCP Commonly Used For

- Web Applications
- APIs
- Database Systems
- Cloud Services
- Enterprise Applications

---

### UDP Commonly Used For

- Streaming Platforms
- Voice Services
- DNS Services
- Gaming Platforms
- Real-Time Communication

---

## Production Engineering Perspective

### Common Challenges

- Network Latency
- Packet Loss
- Connection Timeouts
- Retransmission Overhead
- Application Performance Issues

---

## Most Asked Questions

1. What is TCP?
2. What is UDP?
3. TCP vs UDP?
4. Why is TCP reliable?
5. Why is UDP faster?
6. When should TCP be used?
7. When should UDP be used?
8. Which protocol is used by DNS?

---

## Quick Revision

### Priority

⭐⭐⭐⭐⭐ Highest Priority

### Remember

- TCP provides reliable communication.
- UDP provides faster communication.
- TCP uses acknowledgements and retransmissions.
- UDP minimizes communication overhead.
- TCP is common for web applications and databases.
- UDP is common for streaming, gaming, and DNS.