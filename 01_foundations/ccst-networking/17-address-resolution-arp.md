# ARP Process

## MAC and IP

When a host needs to send a message but only knows the destination's IP address, it must also determine the corresponding MAC address.

In an Ethernet LAN, each device has:
- A **physical address (MAC)** — for NIC-to-NIC communication on the LAN
- A **logical address (IP)** — to send a packet from the source device to the destination, whether on the same IP network or a remote one

A Layer 2 Ethernet frame includes:
- Destination MAC address
- Source MAC address

A Layer 3 IP packet includes:
- Source IPv4 address
- Destination IPv4 address

If the destination IP is on a remote network, the MAC address used is that of the **default gateway** (router interface). The router:
- Receives the Ethernet frame
- De-encapsulates Layer 2 information
- Uses the IP destination address to determine the next-hop device
- Re-encapsulates the IPv4 packet in a new data-link frame for the outgoing interface

> If the next-hop device is the final destination, the destination MAC is that of the target NIC.

- IPv4 → uses the **Address Resolution Protocol (ARP)**
- IPv6 → uses **ICMPv6 Neighbor Discovery (ND)**

---

## Broadcast Domain and ARP

- A host accepts a message addressed to the broadcast MAC (FF:FF:FF:FF:FF:FF).
- Broadcast frames are forwarded by switches to all ports, creating a **broadcast domain**.
- Too many hosts in a single domain → excessive traffic → reduced efficiency.

➡️ LANs are split into **subnets** using **routers** to manage broadcast traffic.

---

## ARP in Action

When a host only knows the destination IP:
1. It sends a **broadcast Ethernet frame** with an ARP Request asking “Who has this IP?”.
2. All devices receive it, but only the one with the matching IP replies with its **MAC address**.
3. The sender saves the mapping in its **ARP table** and can now send unicast frames directly.

---

## Notes

- ARP works only within the **local subnet** (broadcast domain).
- If the destination is remote, the ARP request targets the default gateway's IP instead.
