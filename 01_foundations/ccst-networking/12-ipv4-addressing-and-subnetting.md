# 12 – IPv4 Addressing

---

## Purpose of an IPv4 Address

Every host needs an IPv4 address to access the internet or communicate within most LANs.
An **IPv4 address** is a logical identifier assigned to a device's **Network Interface Card (NIC)**.

Routers that connect devices to an IP network also have IPv4 addresses.
Every packet sent over the internet includes:

- A **source IPv4 address**
- A **destination IPv4 address**

These are essential for routing traffic and ensuring responses return to the correct sender.

> IPv4 addresses are **32 bits** long (4 bytes)

---

## Structure of an IPv4 Address

IPv4 addresses are **hierarchical** and contain two main parts:

- **Network part** (typically the first three decimal blocks)
- **Host part** (the last decimal block)

> The network portion identifies the host's LAN and is the same for all hosts on that network.

---

## Example

```
IP Address: 192.168.1.10
Subnet Mask: 255.255.255.0
```

- Network part: `192.168.1`
- Host part: `10`

This allows routers and switches to determine which part of the address defines the **local network**, and which identifies a **specific device**.

---

> ✅ IPv4 addressing enables logical routing and host identification across diverse networks.
---

📎 **See also:** [Appendix A – CIDR](./appendix_a_cidr.md)
