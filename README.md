# Windows Security Labs

A hands-on portfolio of Windows endpoint security, Active Directory administration, and security monitoring labs. This repository documents how I applied Windows security concepts in controlled environments and connected administrative activity to the logs a SOC analyst would investigate.

> These labs were completed in controlled TryHackMe environments. Credentials, target addresses, flags, and other sensitive lab information are not included.

## Labs

| Lab | Focus | Skills demonstrated |
|---|---|---|
| [Windows Security Fundamentals](windows-fundamentals.md) | Windows endpoint controls and security features | UAC, permissions, patch awareness, BitLocker, TPM, firewall profiles, processes, services, and system monitoring |
| [Windows Active Directory Administration](active-directory-administration.md) | Managing and securing a Windows domain | AD Users and Computers, OUs, delegated permissions, least privilege, PowerShell, Group Policy, Kerberos, and NTLM |
| [Monitoring Active Directory with Splunk](monitoring-active-directory.md) | Investigating identity and authentication activity | SPL, Windows Security Event Logs, Kerberos and NTLM monitoring, account lifecycle events, group changes, baselining, anomaly detection, and event correlation |

## Featured Work

### Active Directory administration

- Cleaned up and reorganized an existing domain structure.
- Delegated password-reset permissions without granting Domain Administrator access.
- Used PowerShell to reset a user password and require a password change at the next sign-in.
- Separated workstations and servers into policy-ready Organizational Units.
- Created and linked Group Policy Objects to restrict Control Panel access and enforce automatic screen locking.
- Reviewed password, account-lockout, Kerberos, tree, forest, and trust concepts.

### Active Directory monitoring

- Queried Windows authentication and account-management events in Splunk.
- Compared Kerberos and NTLM activity across Domain Controllers and endpoints.
- Monitored account creation, password resets, lockouts, and security-group membership changes.
- Distinguished computer-account traffic from human-user activity to reduce noise.
- Used stack counting and baselining to identify rare activity for further investigation.
- Correlated account creation, group assignment, and first authentication events into an onboarding timeline.
- Reviewed Windows audit policies to identify potential visibility gaps.

## Security Events Covered

| Event ID | Description |
|---:|---|
| 4624 / 4625 | Successful and failed logons |
| 4720 | User account created |
| 4724 | Password reset attempted |
| 4728 / 4732 / 4756 | Member added to a security group |
| 4740 | User account locked out |
| 4768 | Kerberos Ticket Granting Ticket requested |
| 4769 | Kerberos service ticket requested |
| 4771 | Kerberos pre-authentication failed |
| 4776 | NTLM credential validation |
| 5136 | Active Directory object modified |
| 5140 | Network share accessed |

## Tools and Technologies

- Splunk Enterprise and SPL
- Windows Security Event Logs
- Active Directory Domain Services
- Active Directory Users and Computers
- Group Policy Management
- Windows PowerShell
- Advanced Audit Policy Configuration
- Kerberos and NTLM
- Remote Desktop and FreeRDP

## Repository Structure

```text
windows-security-labs/
├── README.md
├── windows-fundamentals.md
├── active-directory-administration.md
├── monitoring-active-directory.md
└── images/
```

## Key Takeaway

These labs strengthened my understanding of both sides of Windows security: how administrators configure identities, permissions, computers, and policies, and how analysts monitor the resulting authentication and directory activity. That connection is important when investigating suspicious logons, unauthorized account changes, privilege escalation, persistence, and policy modifications.

## Disclaimer

This repository is for education and portfolio demonstration only. All activity was performed in authorized lab environments.
