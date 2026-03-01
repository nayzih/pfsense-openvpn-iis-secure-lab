# IP Addressing Plan

## LAN

| Equipment     | IP Address       | Role        |
|--------------|-----------------|------------|
| pfSense LAN  | 192.168.100.1   | Gateway    |
| IIS Server   | 192.168.100.10  | Web Server |
| Client       | DHCP            | Internal Workstation |

Network: 192.168.100.0/24

---

## WAN

Interface configured in DHCP (Bridged mode)

---

## VPN

Tunnel network: 10.10.10.0/30 per client

Topology: net30  
Each VPN client is isolated in a distinct subnet.

---

## Security

- No internal service directly exposed
- Controlled publication via NAT
- Remote access only via SSL VPN