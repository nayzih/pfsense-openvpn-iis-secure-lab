# Test – SSL VPN Connection

## Objective

Validate secure remote access via OpenVPN.

---

## Steps

1. Install the OpenVPN client on Windows 10.
2. Import the configuration file (.ovpn).
3. Connect via WAN.
4. Enter user credentials.
5. Verify the OpenVPN icon (green).

---

## Observed Results

- VPN tunnel successfully established.
- IP address 10.10.10.x assigned.
- /30 subnet assigned (client isolation).

Command used:

ipconfig

Confirmation of the virtual TAP interface.

---

## Access to Internal Resources

After connection:

- Access to http://192.168.100.10 is possible.
- Access to other LAN services is blocked.

---

## Security Validation

- Certificate + password authentication.
- Client isolation confirmed.
- Traffic encrypted via AES-256.