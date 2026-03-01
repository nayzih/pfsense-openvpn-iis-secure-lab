# Firewall Rules – OpenVPN Interface

## Objective

Control VPN client access to internal resources.

---

## Rule 1 – Allow HTTP Access to IIS Server

- Action: Pass
- Interface: OpenVPN
- Protocol: TCP
- Source: Any
- Destination: 192.168.100.10
- Port: 80
- Description: Allow OpenVPN to IIS HTTP

### Justification

Allows remote users to access only the internal Web service.  
Other services remain inaccessible.

---

## Applied Security

- VPN client isolation via net30 topology
- SSL/TLS + User authentication
- AES-256 encryption
- auth-nocache enabled