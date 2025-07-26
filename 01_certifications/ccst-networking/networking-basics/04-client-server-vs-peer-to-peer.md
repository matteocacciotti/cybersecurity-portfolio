# Client-Server vs Peer-to-Peer Models

Understanding how devices interact is essential when performing enumeration or lateral movement.

## Client-Server Architecture

- **Client** → Requests resources (e.g., web browser)
- **Server** → Provides resources/services (e.g., web server)
- **Roles are defined by the software**, not hardware

## Peer-to-Peer (P2P) Architecture

- Devices (hosts) act as both clients and servers.
- Common in:
  - File sharing apps
  - Decentralized platforms
- Trade-offs:
  - ❌ Poor scalability
  - ❌ Weak centralized control
  - ❌ Inconsistent security

## Hybrid P2P

- Decentralized sharing with a centralized directory or index server.
- Seen in modern file sharing and blockchain networks.

## Multi-Role Hosts

- A single host can run multiple client and server applications (e.g., a web browser and a local HTTP server).
