# Test – Internal LAN Access

## Objective

Verify that the IIS server is accessible only from the authorized internal network.

---

## Steps

1. From a LAN machine:
   - Access http://192.168.100.10
2. Verify that the default IIS page loads.

---

## Expected Result

- The IIS page displays correctly.
- Communication is allowed via the dedicated LAN rule.
- No other service is accessible.

---

## Security Validation

- Internal DNS functioning.
- External DNS blocking confirmed.
- Access limited to port 80 only.