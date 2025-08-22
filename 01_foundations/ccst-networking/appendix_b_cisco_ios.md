## Appendix B – Cisco IOS Basic Commands

**Cisco IOS** (Internetwork Operating System) is the proprietary operating system used on most Cisco network devices, such as routers and switches. It provides the command-line interface (CLI) that network administrators use to configure, monitor, and troubleshoot devices.  

The following table lists common Cisco IOS commands along with their descriptions.

| Command | Description |
|---------|-------------|
| `show ip interface brief` | Displays interfaces, assigned IP addresses, and their status. |
| `show vlan brief` | Lists configured VLANs and assigned ports. |
| `show mac address-table` | Displays the MAC address table learned by the switch. |
| `show ip route` | Shows the IPv4 routing table. |
| `show version` | Displays device information and Cisco IOS version. |
| `show running-config` | Displays the current active configuration. |
| `show startup-config` | Displays the configuration stored in NVRAM that loads at startup. |
| `line console 0` | Enters configuration mode for the console line. |
| `password <pw>` + `login` | Sets a console or VTY access password. |
| `enable password <pw>` | Sets an unencrypted privileged mode password. |
| `enable secret <pw>` | Sets an encrypted privileged mode password. |
| `line vty 0 4` | Configures remote access via Telnet/SSH. |
| `service password-encryption` | Encrypts visible passwords in the configuration. |
| `ip default-gateway <IP>` | Sets the default gateway on a Layer 2 switch. |
| `interface vlan 1` + `ip address <IP> <mask>` + `no shutdown` | Assigns an IP address to the management VLAN. |
