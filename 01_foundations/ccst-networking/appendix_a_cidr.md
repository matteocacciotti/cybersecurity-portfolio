## Appendix A – CIDR Notation and Subnet Calculations (/24 to /30)

The following table summarizes the relationship between CIDR notation, subnet masks, block sizes, and the calculation of usable hosts for common subnet sizes.  
The “Usable Hosts” column excludes the network and broadcast addresses.

**Block Size** refers to the number of IP addresses contained within a subnet.  
It is calculated by subtracting the subnet mask's value in the last octet from 256.

| CIDR | Subnet Mask       | Block Size Calculation  | Usable Host Calculation            |
|------|-------------------|-------------------------|-------------------------------------|
| /24  | 255.255.255.0     | 256 − 0 = 256           | Block size = 256 → 256 − 2 = 254 hosts |
| /25  | 255.255.255.128   | 256 − 128 = 128         | Block size = 128 → 128 − 2 = 126 hosts |
| /26  | 255.255.255.192   | 256 − 192 = 64          | Block size = 64 → 64 − 2 = 62 hosts   |
| /27  | 255.255.255.224   | 256 − 224 = 32          | Block size = 32 → 32 − 2 = 30 hosts   |
| /28  | 255.255.255.240   | 256 − 240 = 16          | Block size = 16 → 16 − 2 = 14 hosts   |
| /29  | 255.255.255.248   | 256 − 248 = 8           | Block size = 8 → 8 − 2 = 6 hosts      |
| /30  | 255.255.255.252   | 256 − 252 = 4           | Block size = 4 → 4 − 2 = 2 hosts      |
