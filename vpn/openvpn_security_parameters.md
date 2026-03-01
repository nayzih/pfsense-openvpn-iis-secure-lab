# Security Parameters – OpenVPN

## Encryption

- Encryption Algorithm: AES-256-CBC
- Auth Digest: SHA256
- TLS Authentication enabled

---

## Additional Protection

Added directive:

auth-nocache

Prevents credential caching on the client workstation.

---

## Client Isolation

Topology: net30

Each client receives:

- Dedicated /30 subnet
- No inter-client communication possible

---

## Restricted Access

OpenVPN Interface:

- Allow HTTP to 192.168.100.10 only
- No full LAN access

Least privilege principle applied.

---

## Logs and Monitoring

- OpenVPN logs enabled
- Monitoring via Status > OpenVPN
- Possible SIEM integration

---

## Possible Improvements

- MFA (OTP)
- Short-lived certificates (1 year)
- TLS 1.3 only
- Source IP limitation
- Fail2ban