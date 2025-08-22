# 16 – Gateways, NAT & Private-to-Public Routing

---

## Gateway Definition

A **gateway** allows devices in one network to communicate with devices in another.
On IP networks, this is typically the **default gateway** — the IP of the router's internal interface.

---

## Router Roles

- Home router acts as:
  - **DHCP server** (for internal clients)
  - **DHCP client** (to the ISP)
- Internal IPs are private and **not routable** on the public internet.
- ISP assigns the router a **routable public IPv4 address**, which is shared among LAN devices.

---

## NAT – Network Address Translation

**NAT** enables devices with private IPs to communicate externally by:

- Translating the internal IP to the router’s public IP
- Recording mappings in a NAT table
- Reversing the process for inbound traffic

---

## PDU – Protocol Data Unit

A **PDU** is the smallest chunk of data handled at each layer of the OSI or TCP/IP model.
Examples:
- Bits (physical layer)
- Frames (data link layer)
- Packets (network layer)
- Segments (transport layer)
