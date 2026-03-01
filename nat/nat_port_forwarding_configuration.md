# NAT Configuration – Port Forwarding

## Objective

Allow access to the internal Web server (IIS) from outside the network via the WAN interface, while maintaining strict traffic control.

The internal server must never be directly exposed.

---

## NAT Principle (Network Address Translation)

Port Forwarding allows:

- Receiving incoming traffic on a public address (WAN)
- Redirecting this traffic to an internal server
- Masking internal addressing

In this project:

Internet → pfSense WAN → NAT → IIS Server (192.168.100.10)

---

## Applied Configuration

Menu: `Firewall > NAT > Port Forward`

### Parameters:

- Type: Port Forward
- Interface: WAN
- Protocol: TCP
- Destination: WAN address
- Destination Port: 80 (HTTP)
- Redirect Target IP: 192.168.100.10
- Redirect Target Port: 80
- Description: NAT WAN to IIS HTTP

---

## Operation

1. An external client accesses the WAN IP address of pfSense.
2. pfSense intercepts the HTTP request (TCP 80).
3. The NAT rule redirects it to 192.168.100.10.
4. The IIS server responds.
5. pfSense forwards the response back to the external client.

---

## Applied Security

- Only port 80 is forwarded.
- No other internal service is exposed.
- The server remains within the LAN (non-public).
- WAN firewall rules control access.
- Source IP restriction can be added.

---

## Associated Risks

Exposing a service via NAT implies:

- Increased attack surface
- Risk of IIS vulnerability exploitation
- Automated scanning attempts

---

## Possible Improvements

- HTTPS publication (443)
- Reverse proxy implementation
- Source IP limitation
- DMZ deployment
- IDS/IPS activation
- WAN log monitoring

---

## Conclusion

The NAT configuration enables controlled publication of the internal Web service.

The pfSense firewall ensures:

- Address translation
- Incoming traffic filtering
- Control of service exposure