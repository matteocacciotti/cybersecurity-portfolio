# Inter-Network Routing

## Why Routing Is Needed

When devices communicate beyond their local subnet, they require **routers** to forward packets across networks.

A **router** is a Layer 3 device that:
- Connects multiple IP networks
- Makes forwarding decisions based on the **destination IP address**

---

## Routing vs Switching

| Switch (L2)         | Router (L3)             |
|---------------------|-------------------------|
| Uses MAC addresses  | Uses IP addresses       |
| Operates within LAN | Connects different LANs |

Routers:
- Read the **network portion** of the destination IP
- Decide the best outgoing interface or next-hop device

---

## The Routing Table

Routers maintain a **routing table**:
- Lists known networks
- Maps them to specific interfaces or next-hop routers

Types of routes:
- **Directly connected** (on one of the router's interfaces)
- **Static** (manually configured)
- **Dynamic** (learned via routing protocols)

If no match is found, and no **default route** exists, the packet is dropped.

---

## Default Gateway

On end devices:
- The **default gateway** is the router used to reach other networks
- Its IP is configured in the host's TCP/IP settings

To send a packet:
- The host uses ARP to resolve the MAC of the gateway IP
- The frame is addressed to the router’s MAC

---

## LAN Design

A **LAN** (Local Area Network):
- May span a single location or multiple branches
- Uses Ethernet or wireless protocols
- Offers high-speed communication under a single admin domain

---

### Intranet

A private LAN accessible only to authorized users within an organization.

---

### Local vs Remote Segments

LAN hosts can be grouped as:
1. **Single subnet (flat LAN)**:
   - All hosts share the same broadcast domain
   - Simpler and faster communication, but more congestion

2. **Multiple subnets (segmented LAN)**:
   - Each subnet has fewer hosts
   - Requires routing between segments
   - Improves performance and security
