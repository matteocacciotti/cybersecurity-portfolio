# 09 – Communication Principles

---

## Communication Protocol Requirements

Communication protocols define **rules for exchanging data** between devices. They require:

- A method of initiation and control
- A shared language and format
- Confirmation and acknowledgment mechanisms

### Network Protocols Specify:

- Message format and size
- Timing and synchronization
- Data encoding
- Encapsulation: adding a header with addressing info (origin and destination)

> MAC (Media Access Control): a unique identifier assigned to each network interface card by the manufacturer

> A typical Ethernet frame carries between 64 and 1518 bytes of data.

---

## Protocol Stack – TCP/IP Model

When a device sends a message, it follows a layered set of protocols known as the **protocol stack**, typically TCP/IP:

- **Application Layer**
  - Example: HTTP (*HyperText Transfer Protocol*)
  - Used between browsers and web servers to request and receive HTML files

- **Transport Layer**
  - Example: TCP (*Transmission Control Protocol*)
  - Ensures reliable delivery, packet sequencing, and error correction

- **Internet Layer**
  - Example: IP (*Internet Protocol*)
  - Handles addressing and routing between networks

- **Network Access Layer**
  - Defines physical transmission over the network medium

> Each layer relies on the services provided by the layer below.

