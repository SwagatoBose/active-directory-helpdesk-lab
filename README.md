# Active Directory Help Desk & Windows Administration Lab

A hands-on home lab built to practice **Windows administration**, **Active Directory**, **Group Policy**, **DNS**, **networking**, and **help-desk troubleshooting**.

---

## Lab Environment

| Component              | Details                          |
|------------------------|----------------------------------|
| Hypervisor             | Oracle VirtualBox                |
| Domain Controller      | Windows Server 2025 (`DC01`)     |
| Client                 | Windows 11 (`AcerLap`)           |
| Domain                 | `corp.local`                     |
| Directory Services     | Active Directory Domain Services (AD DS) |
| Name Resolution        | DNS                              |
| Automation / Scripting | PowerShell                       |
| Policy Management      | Group Policy Management Console  |

---

## Lab Architecture

Internet
  → VirtualBox NAT
    → Windows 11 (AcerLap) - 10.0.2.15
      → Internal Network (AD-LAB)
        → DC01 (Windows Server) - 192.168.10.10
          - AD DS
          - DNS

---

## Network Configuration

| Host       | Role                  | IP Address     | Network Adapter      |
|------------|-----------------------|----------------|----------------------|
| DC01       | Domain Controller     | 192.168.10.10  | Internal Network (AD-LAB) |
| AcerLap    | Domain-joined Client  | 10.0.2.15      | NAT + Internal Network |

---

## Goals

- Build and maintain a functional Active Directory domain
- Practice day-to-day help-desk and system administration tasks
- Configure and troubleshoot Group Policy
- Manage DNS and basic networking
- Automate common tasks with PowerShell

---

## Getting Started

1. Clone this repository
2. Review the lab architecture above
3. Deploy the virtual machines in VirtualBox
4. Follow the setup notes (to be added) for promoting `DC01` and joining the client to the domain

---

## License

This lab is for educational and personal use only.
