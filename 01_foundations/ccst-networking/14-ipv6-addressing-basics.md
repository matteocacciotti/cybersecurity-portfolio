# 14 – IPv6 Addressing Formats & Transition Strategies

---

## IPv4 Limitations

- IPv4 is a 32-bit system → ~4.3 billion addresses.
- IPv6 is 128-bit → ~3.4 x 10^38 possible addresses.
- IPv6 supports:
  - Native auto-configuration
  - Enhanced peer-to-peer communication (no NAT required)
  - Modern scalability for mobile and IoT devices

---

## Transition to IPv6

Operators and ISPs have already moved the majority of traffic to IPv6 in many countries.

### Transition Technologies

- **Dual Stack** → Devices run IPv4 and IPv6 simultaneously.
- **Tunneling** → Encapsulates IPv6 packets inside IPv4 for transport across IPv4-only networks.
- **Translation (NAT64)** → Enables communication between IPv4 and IPv6 devices using translation techniques.

> Tunneling and translation should be transitional — native IPv6 is the long-term goal.

---

## IPv6 Address Format

- Expressed in hexadecimal (base-16)
- 128 bits total → 8 groups of 4 hex digits each → known as **hextets**

Example:
```
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

---

## IPv6 Notation Rules

- **Rule 1**: Omit leading zeroes in any hextet.
- **Rule 2**: Use double colons `::` to replace one contiguous sequence of all-zero hextets (only once per address).
