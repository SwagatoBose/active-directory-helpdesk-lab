# Ticket 10 — Domain Password Policy Configuration

## Scenario

The organization requested stronger password requirements for domain users.

The domain password policy was configured through the Default Domain Policy.

---

## Environment

- Domain Controller: `DC01`
- Client: `AcerLap`
- Domain: `corp.local`

---

## Requirements

The following password policy was required:

- Password history: 5 passwords
- Maximum password age: 60 days
- Minimum password age: 1 day
- Minimum password length: 8 characters
- Password complexity: Enabled

---

## Configuration

The password policy was configured on `DC01` using:

**Group Policy Management → Default Domain Policy**

Path:

`Computer Configuration → Policies → Windows Settings → Security Settings → Account Policies → Password Policy`

The required password settings were configured according to the requested policy.

---

## Verification

The Windows 11 client was refreshed using:

```powershell
gpupdate /force
