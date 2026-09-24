# Ticket 10 — Domain Password Policy Configuration

## Scenario

The organization requested stronger password requirements for domain users.

The help desk configured the domain password policy through the Default Domain Policy and verified that the settings were applied successfully.

---

## Environment

- Domain Controller: `DC01`
- Client: `AcerLap`
- Domain: `corp.local`

---

## Problem

The existing domain password policy did not meet the organization's required password security standards.

The following password requirements were requested:

- Password history: 5 passwords
- Maximum password age: 60 days
- Minimum password age: 1 day
- Minimum password length: 8 characters
- Password complexity: Enabled

---

## Troubleshooting

1. Opened **Group Policy Management** on `DC01`.
2. Edited the **Default Domain Policy**.
3. Navigated to:
   `Computer Configuration → Policies → Windows Settings → Security Settings → Account Policies → Password Policy`
4. Configured the required password policy settings.
5. Ran `gpupdate /force` on the Windows 11 client.
6. Verified the domain password policy using:
   `net accounts /domain`

---

## Resolution

The domain password policy was configured with the required password security settings.

The policy was successfully refreshed on the Windows 11 client and the configured values were verified.

---

## Verification

The domain password policy was verified using:

```cmd
net accounts /domain
