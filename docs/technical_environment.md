# Technical Environment

## Virtualization

Platform: VMware Workstation

Allows simulation of a complete infrastructure without physical hardware.

---

## Firewall

- pfSense Community Edition
- 2 network interfaces (WAN / LAN)
- ZFS (default installation)

---

## Web Server

- Windows Server 2022
- IIS role enabled
- HTTP publication (port 80)

---

## VPN

- OpenVPN integrated into pfSense
- Remote Access mode (SSL/TLS + User Auth)
- AES-256 encryption
- Certificate + password authentication

---

## Client Workstation

- Windows 10 Professional
- OpenVPN Community Client
- Remote connection via WAN