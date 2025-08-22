# Wireshark and Packet Analysis

## Introduction
Wireshark is a free and open-source network protocol analyzer that allows you to capture and inspect packets in real-time or from saved capture files (.pcap). It is an essential tool for network troubleshooting, performance monitoring, and security analysis.

In the context of the **CCST Networking** exam, Wireshark is relevant for:
- Capturing network packets
- Filtering traffic by protocol, IP, or port
- Analyzing common protocols (HTTP, DNS, ICMP)
- Identifying potential network issues

---

## Basic Concepts

### Promiscuous Mode
A network interface mode that allows the NIC to receive all packets that pass through the network segment, regardless of the intended destination MAC address.

### Filter Types
- **Capture Filters**: Applied before packet capture to limit what is collected (e.g., `port 80`).
- **Display Filters**: Applied after capture to focus on specific traffic (e.g., `http`, `ip.addr == 192.168.1.10`).

### Packet Structure
1. **Ethernet Header** – Source/Destination MAC addresses
2. **IP Header** – Source/Destination IP addresses
3. **TCP/UDP Header** – Source/Destination ports
4. **Application Data** – Protocol-specific content

---

## Practical Exercises

### 1. HTTP Traffic Analysis
- Filter: `http`
- Goal: Identify GET requests and the IP addresses of contacted hosts

Output: [01-http_request_get.png](images/01-http_request_get.png)

### 2. DNS Query Analysis
- Filter: `dns`
- Goal: Identify domain names queried and corresponding IP addresses returned

Output: [02-dns_query_example_com.png](images/02-dns_query_example_com.png); [03-dns_response_example_com.png](images/03-dns_response_example_com.png)

### 3. ICMP Ping Analysis
- Filter: `icmp`
- Goal: Count Echo Request and Echo Reply packets

Output: [04-icmp_request_ping.png](images/04-icmp_request_ping.png); [05-icmp_reply_ping.png](images/05-icmp_reply_ping.png)

---

## Example Report Output

**HTTP Example**:
```
Protocol: HTTP GET
Source: 192.168.1.10
Destination: 172.217.22.14
Port: 80
```
**DNS Example**:
```
Protocol: DNS Query
Domain: example.com
Returned IP: 93.184.216.34
```
