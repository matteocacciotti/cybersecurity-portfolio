# Network Troubleshooting Commands

This section lists essential command-line tools used to diagnose and solve basic networking problems. These are commonly used in CCST Networking and other entry-level certifications.

---

## IP Configuration Tools

| Command              | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| `ipconfig`           | Displays IP address, subnet mask, and default gateway (Windows)            |
| `ipconfig /all`      | Shows detailed IP information, including MAC and DNS servers                |
| `ipconfig /release`  | Releases current DHCP-assigned IP address                                   |
| `ipconfig /renew`    | Requests a new IP address from the DHCP server                              |
| `ifconfig`           | Linux/macOS equivalent to `ipconfig`                                        |

---

## DNS Troubleshooting

| Command               | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| `nslookup domain.com` | Queries DNS to find the IP address of a domain                             |
| `dig domain.com`      | Advanced DNS query tool (Linux/macOS)                                      |

---

## Connection Testing

| Command                 | Description                                                              |
|-------------------------|--------------------------------------------------------------------------|
| `ping <ip or domain>`   | Tests network connectivity and latency                                   |
| `tracert <domain>`      | Traces the route packets take to a destination (Windows)                |
| `traceroute <domain>`   | Unix/Linux/macOS equivalent of `tracert`                                 |

---

## Port and Socket Monitoring

| Command         | Description                                                                    |
|-----------------|--------------------------------------------------------------------------------|
| `netstat`       | Lists active TCP connections and ports in use                                 |
| `netstat -n`    | Displays connections using numeric IPs and ports                              |
| `netstat -a`    | Shows all listening ports and active connections                              |
| `netstat -b`    | Shows executable associated with each connection (Windows, requires admin)    |

---

## ARP and MAC Address Tools

| Command       | Description                                                                    |
|---------------|--------------------------------------------------------------------------------|
| `arp -a`      | Displays the ARP table: IP-to-MAC mappings                                     |
| `getmac`      | Displays the MAC address of the system's network interfaces                    |

---

## Routing and Network Status

| Command         | Description                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| `route print`   | Displays the local routing table (Windows)                                  |
| `ip route show` | Shows routing table on Linux                                                |
| `hostname`      | Displays or sets the system hostname                                        |
| `netsh`         | Windows utility to configure and reset network settings                     |

---

## Additional Tools

| Command              | Description                                                           |
|----------------------|-----------------------------------------------------------------------|
| `telnet <host> <port>` | Tests open TCP port connections (legacy and insecure, for testing) |
| `ssh <user>@<host>`  | Secure remote terminal access                                        |
| `ftp`                | Transfers files over TCP (use SFTP for secure transfer)              |
---

📎 **See also:** [Appendix B – Cisco IOS Commands](./appendix_b_cisco_ios.md)
