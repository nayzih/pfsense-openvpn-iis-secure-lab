# Logical Architecture

## Objective

Implement a segmented network architecture simulating a secure corporate environment.

---

## Network Segmentation

The infrastructure is based on two main zones:

### WAN
- Interface configured in Bridged mode
- Simulates Internet access
- Untrusted zone

### LAN
- Isolated internal network
- 192.168.100.0/24
- Hosts the IIS Web server

---

## Perimeter Security

The pfSense firewall ensures:

- Routing between WAN and LAN
- Traffic filtering
- Address translation (NAT)
- SSL VPN termination

---

## Main Components

- pfSense (firewall)
- Windows Server 2022 (IIS)
- Windows 10 (VPN client)
- OpenVPN SSL

---

## Applied Principles

- Network segmentation
- Least privilege principle
- VPN client isolation
- Communication encryption