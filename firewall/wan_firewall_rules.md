# Firewall Rules – WAN Interface

## Objective

Allow only necessary external connections.

The WAN is considered an untrusted zone.

---

## Rule 1 – Allow OpenVPN

- Action: Pass
- Interface: WAN
- Protocol: UDP
- Destination: WAN address
- Port: 1194 (or custom port)
- Description: Allow OpenVPN Remote Access

### Justification

Allows establishment of the SSL VPN tunnel from external sources.  
No other inbound service is directly authorized.