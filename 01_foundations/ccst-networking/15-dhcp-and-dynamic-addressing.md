# 15 – Dynamic Addressing with DHCP

---

## Static vs Dynamic Addressing

### Static IPv4

- Manually configured:
  - IP address
  - Subnet mask
  - Default gateway
- Suitable for:
  - Servers
  - Printers
  - Devices requiring consistent availability
- Risk: human error during configuration

> Keep a detailed inventory of statically assigned addresses.

---

### Dynamic IPv4 – DHCP

- **DHCP (Dynamic Host Configuration Protocol)** automates:
  - IP address assignment
  - Subnet mask
  - Gateway information
- Common in large networks; addresses are leased and returned to the **IP pool** when no longer in use.

---

## DHCP Operation

1. **DHCP Discover** – Host broadcasts a request (includes its MAC)
2. **DHCP Offer** – Server responds with available IP and config
3. **DHCP Request** – Host accepts the offer
4. **DHCP ACK** – Server confirms lease

> Used by routers (home networks) or dedicated servers (enterprise)