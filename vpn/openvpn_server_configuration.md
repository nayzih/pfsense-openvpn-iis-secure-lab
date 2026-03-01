# OpenVPN Server Configuration

## Objective

Allow secure remote access to the internal LAN network through an encrypted tunnel.

---

## Menu

VPN > OpenVPN > Servers

---

## Main Parameters

- Server Mode: Remote Access (SSL/TLS + User Auth)
- Protocol: UDP
- Port: 1194
- Interface: WAN
- Peer Certificate Authority: CA-OPENVPN
- Server Certificate: Created server certificate

---

## VPN Network

- IPv4 Tunnel Network: 10.10.10.0/24
- Topology: net30 (client isolation)
- Redirect Gateway: Disabled (Split Tunnel)

---

## Accessible Local Network

- IPv4 Local Network: 192.168.100.0/24

Allows VPN clients to access the internal LAN.

---

## Client Export

Installed package:

- openvpn-client-export

Allows generation of:

- .ovpn file
- Complete archive
- Configuration compatible with OpenVPN Community

---

## Operation

1. Remote client connects via WAN.
2. TLS tunnel established.
3. Tunnel IP assigned.
4. Controlled access via OpenVPN firewall rules.