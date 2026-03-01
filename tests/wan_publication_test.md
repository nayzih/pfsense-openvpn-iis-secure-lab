# Test – WAN Publication via NAT

## Objective

Validate that the internal Web server is accessible from outside via the configured NAT rule.

---

## Steps

1. From an external machine (WAN):
   - Access the WAN IP address of pfSense
   - Port: 80
2. Observe the behavior.

---

## Expected Result

- The internal IIS page is displayed.
- The request is redirected via NAT to 192.168.100.10.
- No other port is accessible.

---

## Additional Verifications

- Nmap scan on the WAN IP:
  - Only ports 80 and 1194 (OpenVPN) are visible.
- No direct access to the LAN.

---

## Controlled Risk

Publication is limited to the strict minimum.  
The server remains not directly exposed.