# PKI Infrastructure – OpenVPN

## Objective

Implement a certificate infrastructure to secure VPN authentication.

---

## Principle

The SSL VPN relies on:

- A Certificate Authority (CA)
- A server certificate
- A user certificate

This ensures:

- Strong authentication
- TLS encryption
- Protection against Man-in-the-Middle attacks

---

## Certificate Authority

Menu: `System > Certificates > Authorities`

Configuration:

- Method: Create an internal Certificate Authority
- Name: CA-OPENVPN
- Key: 2048 or 4096 bits
- Duration: 10 years

---

## Server Certificate

Menu: `System > Certificates > Certificates`

- Type: Server Certificate
- Certificate Authority: CA-OPENVPN
- Usage: Server Authentication
- Duration: 3650 days

Used to:

- Identify the VPN server
- Establish the TLS tunnel

---

## User Certificate

Menu: `System > User Manager`

- Create local user
- Generate associated user certificate
- Signed by internal CA

Used to:

- Authenticate the client
- Secure VPN access

---

## Security Provided

- Logical dual-factor authentication (certificate + password)
- Protection against impersonation
- Cryptographic server validation