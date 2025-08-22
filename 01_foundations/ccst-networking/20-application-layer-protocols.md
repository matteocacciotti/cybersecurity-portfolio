# Application Layer Services

## Client–Server Interaction

Web services and APIs use **URIs (Uniform Resource Identifiers)** to locate resources.

### URI Types:
- **URN (Name)** → identifies a resource without implying location
- **URL (Locator)** → specifies the location of the resource

### URL Structure:
```
protocol://hostname/path/to/resource
```
Example:
```
https://example.com/docs/page.html
```

---

## Domain Name System (DNS)

DNS maps **domain names** to **IP addresses**.

When a user types a domain:
- The client DNS resolver asks a DNS server for its IP
- This precedes sending an HTTP request

Command-line tool:
```bash
nslookup example.com
```

For home networks, the DNS server is typically provided via DHCP by the home router.

---

## Web Clients and Servers

### HTTP/HTTPS
- **HTTP (port 80)** → Not secure, readable in transit
- **HTTPS (port 443)** → Secure, uses encryption (TLS/SSL)

Pages are returned in **HTML (Hypertext Markup Language)**:
- A markup language that tells browsers how to render content

---

## FTP – File Transfer Protocol

Used for uploading/downloading files between computers.

- Control connection → port 21
- Data transfer → port 20

Many systems and browsers have built-in FTP clients.
Note: insecure unless used over **SFTP or FTPS**.

---

## Virtual Terminals

### Telnet
- Allows command-line access to a remote device
- Port 23
- **Not encrypted** – vulnerable to interception

### SSH (Secure Shell)
- Secure alternative to Telnet
- Encrypts all communication
- Uses **port 22**

SSH should always be preferred over Telnet for administration.

---

## Email Protocols

Email uses **application-layer protocols** for sending/receiving messages:

| Protocol | Port | Purpose                         |
|----------|------|----------------------------------|
| SMTP     | 25   | Send messages (client → server)  |
| POP3     | 110  | Retrieve & delete from server    |
| IMAP4    | 143  | Retrieve & sync (keeps mail on server) |

Email address format:
```
username@domain.com
```

---

## Messaging and VoIP

### Instant Messaging
- Real-time exchange of text between clients
- Typically web-based or app-specific (e.g., WhatsApp, Slack)

### VoIP – Voice over IP
- Converts voice into digital packets (streamed via UDP)
- May use P2P for direct calls
- To reach traditional phones, a **PSTN gateway** is required
