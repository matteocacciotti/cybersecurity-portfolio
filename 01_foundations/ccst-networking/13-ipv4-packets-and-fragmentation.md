# 13 – IPv4 Addressing & Network Segmentation

## Unicast, Broadcast, and Multicast

- **Unicast** → One-to-one communication; a single source sends to a single destination.
  > IPv4 unicast addresses range from `1.0.0.0` to `223.255.255.255`, with specific ranges reserved for special use.

- **Broadcast** → One-to-all communication within the local network.
  > Uses the destination address `255.255.255.255` (all host bits set to 1). Should be minimized to avoid degrading network performance.

- **Multicast** → One-to-many communication to a selected group of hosts.
  > Uses addresses in the range `224.0.0.0` to `239.255.255.255`. Hosts must join the multicast group to receive packets. Protocols like OSPF use multicast to communicate (e.g., `224.0.0.5` for OSPF routers).

---

## IPv4 Address Types

- **Public Addresses** → Globally routable over the internet.
- **Private Addresses** → Not routable externally; used for internal LANs.

> IPv4 exhaustion led to the adoption of private IP ranges and NAT. The IANA allocates IPv4 blocks to RIRs based on justification.

| Class      | Private Range                    | CIDR Notation    |
|------------|----------------------------------|------------------|
| 🟩 Class A | `10.0.0.0 – 10.255.255.255`       | `10.0.0.0/8`     |
| 🟨 Class B | `172.16.0.0 – 172.31.255.255`     | `172.16.0.0/12`  |
| 🟦 Class C | `192.168.0.0 – 192.168.255.255`   | `192.168.0.0/16` |

---

## Special IPv4 Addresses

- **Loopback** (`127.0.0.0/8`) → Self-addressing for testing (e.g., `ping 127.0.0.1`)
- **Link-Local / APIPA** (`169.254.0.0/16`) → Auto-assigned if DHCP fails
- **Network/Broadcast Addresses** → Reserved for network control and cannot be assigned to hosts

---

## Legacy Classful Addressing

| 🏷️ Class   | 🌍 Range                    | 🔢 First Octet | 🎯 Hosts per Network | 🧠 Intended Use      |
|------------|-----------------------------|----------------|----------------------|----------------------|
| 🟩 A       | `0.0.0.0 – 127.255.255.255` | `0 – 127`      | ≈ 16.7 million       | Large networks       |
| 🟨 B       | `128.0.0.0 – 191.255.255.255`| `128 – 191`    | ≈ 65,534             | Medium networks      |
| 🟦 C       | `192.0.0.0 – 223.255.255.255`| `192 – 223`    | 254                  | Small networks       |

> Class D is reserved for multicast.
> Class E is reserved for experimental use.

---

## IP Address Allocation

- Public IPv4/IPv6 addresses are globally routable and must be unique.
- Managed by **IANA** → assigned to **RIRs** → distributed to **ISPs**.

---

## Network Segmentation

- Broadcast traffic and protocols like **ARP** use Layer 2 broadcasts to locate MACs for IPv4 hosts.
- **DHCP** relies on broadcasts to locate servers.
- **Switches** forward broadcasts on all ports except the incoming one.
- ⚠️ **Routers do not forward broadcasts.**

### Why Subnet?

- Large broadcast domains create unnecessary traffic.
- **Subnetting** breaks a network into smaller logical domains, improving performance and enabling better policy enforcement.

> Subnets can be organized by location, function, or device type.
