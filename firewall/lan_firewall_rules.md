# Firewall Rules – LAN Interface

## Objective

Restrict outbound traffic from the internal network in order to apply the **least privilege** principle.

The LAN must only be able to access strictly necessary services.

---

## Rule 1 – Allow DNS to pfSense

- Action: Pass
- Interface: LAN
- Protocol: TCP/UDP
- Source: LAN net
- Destination: LAN address (pfSense)
- Port: 53
- Description: Allow LAN to pfSense DNS

### Justification

Allows internal machines to use the firewall’s DNS service.  
Prevents the use of uncontrolled external DNS servers.

---

## Rule 2 – Allow HTTP to IIS Server

- Action: Pass
- Interface: LAN
- Protocol: TCP
- Source: LAN net
- Destination: 192.168.100.10
- Port: 80
- Description: Allow LAN to IIS HTTP

### Justification

Allows only HTTP access to the internal Web server.  
No other service is exposed.

---

## Rule 3 – Block External DNS

- Action: Block
- Interface: LAN
- Protocol: TCP/UDP
- Source: LAN net
- Destination: Any
- Port: 53
- Description: Block LAN to External DNS

### Justification

Prevents bypassing the internal DNS.  
Strengthens control over outbound traffic.