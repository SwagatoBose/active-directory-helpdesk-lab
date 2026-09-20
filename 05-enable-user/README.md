# Ticket 05 — Re-enable User Account

## Ticket

> Neha Sharma has returned to the organization. Re-enable her previously disabled Active Directory account and verify that she can authenticate again.

## User Details

- Name: Neha Sharma
- Username: `neha.sharma`
- Domain: `corp.local`
- Domain Controller: `DC01`

## Objective

Re-enable the user's Active Directory account and verify successful domain authentication.

## Procedure

1. Opened **Active Directory Users and Computers** on `DC01`.
2. Located **Neha Sharma**.
3. Used **Enable Account** to re-enable the disabled account.
4. Verified that the account was enabled.
5. Logged into the Windows 11 client using the domain account.
6. Used the `whoami` command to verify the authenticated domain user.

## Verification

The Active Directory account was successfully re-enabled.
The `whoami` command returned:



```text
corp\neha.sharma
