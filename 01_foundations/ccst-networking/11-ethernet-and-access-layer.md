# 11 – Ethernet Frames and Access Layer

---

## Encapsulation and Ethernet Frames

Ethernet is the most common technology used in LANs. Devices connect to the Ethernet LAN via a Network Interface Card (NIC) and are identified by a MAC (Media Access Control) address.

### Ethernet Frame Structure

Each Ethernet frame includes the following fields:

- **Preamble** – 7 bytes
- **Start Frame Delimiter** – 1 byte
- **Destination MAC Address** – 6 bytes
- **Source MAC Address** – 6 bytes
- **Length/Type** – 2 bytes
- **Data (Payload)** – 46 to 1500 bytes
- **FCS (Frame Check Sequence)** – 4 bytes

> Ethernet operates at **Layer 2** of the OSI model (Data Link Layer).

---

## How Ethernet Switches Handle Frames

- A switch builds a **MAC address table** by learning the **source MAC** address of incoming frames.
- If the destination MAC is **not yet known**, the switch **floods** the frame out all ports **except the one it came from**.
- Devices receiving the frame check the **destination MAC**:
  - If it matches their own, they accept it.
  - If not, they ignore the frame.

> This behavior allows the switch to efficiently forward future frames to the correct device once it learns the mapping.

