# TCP and UDP

## Transport Layer Protocols

The **transport layer** divides application data into segments. Each segment includes a header with protocol-specific information.

### TCP – Transmission Control Protocol
- **Connection-oriented**
- Ensures **reliability** with sequence numbers and acknowledgments
- Detects and retransmits lost segments
- Used for: web browsing (HTTP/HTTPS), email (SMTP, IMAP), file transfers (FTP)

### UDP – User Datagram Protocol
- **Connectionless** and **"best-effort"**
- No guarantee of delivery, order, or duplication protection
- Lower latency, ideal for **real-time** applications like:
  - Video/audio streaming
  - Online gaming
  - VoIP

---

## Port Numbers

Every segment includes:
- **Source port** (the sender)
- **Destination port** (the intended service)

Ports identify specific services on a host. Common examples:
- Port 80 → HTTP
- Port 443 → HTTPS
- Port 25 → SMTP

Port ranges:
| Type            | Range         | Use                                         |
|-----------------|---------------|----------------------------------------------|
| Well-known      | 0 – 1023      | Common services (e.g. HTTP, FTP, SSH)       |
| Registered      | 1024 – 49151  | Assigned for user applications              |
| Dynamic/private | 49152 – 65535 | Ephemeral ports, chosen by the client OS    |

Port management is handled by **IANA (Internet Assigned Numbers Authority)**.

---

## Socket Pairs

A **socket** is a combination of:
- IP address + port number

Socket pairs uniquely identify a session:
- `(Source IP : Source Port) → (Dest IP : Dest Port)`

This allows multiple sessions from/to the same IP addresses.

---

## Monitoring Connections: `netstat`

Use `netstat` to check open TCP/UDP connections on a system:
- Displays local/remote IPs and ports, protocol used, and status

Example:
```bash
netstat -n
```
- `-n` shows IPs and ports in numeric form
- Useful for identifying suspicious or unknown connections

Unexplained TCP connections may indicate a **security threat**.
