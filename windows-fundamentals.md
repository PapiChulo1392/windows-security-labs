# Windows Security Fundamentals

## Overview

I completed the Windows Fundamentals 1, 2, and 3 rooms to build a stronger understanding of Windows security features and how they relate to security operations.

This was a fundamentals review rather than a configuration lab. My goal was to understand what normal Windows security controls look like, what areas attackers may try to access or modify, and what information an analyst can review during an investigation.

## User Access Control and Permissions

Windows uses permissions to control what users and applications can access or change.

User Account Control, or UAC, adds an extra approval step before administrative changes can be made. This helps prevent applications from silently modifying important system settings.

From a security perspective, users should only have the permissions required for their role. Excessive administrator access increases the damage that can occur if an account is compromised.

## Boot and System Information

Windows provides tools for reviewing boot settings, startup options, services, and operating system information.

These areas are important because attackers may try to modify startup settings or services to maintain access after a system restarts.

Unexpected boot entries, startup programs, or service changes may require further investigation.

## Windows Updates and Patch Awareness

I learned how to review Windows update history and installation dates.

This introduced me to the basics of patch management. Missing security updates can leave systems exposed to known vulnerabilities.

A security team may need to identify:

- When a system was last updated
- Which patches are missing
- Whether an update installed successfully
- Which systems remain vulnerable

## Shadow Copies and Ransomware Recovery

Windows Shadow Copies can store previous versions of files and system data.

They may help recover files after accidental changes or certain ransomware incidents. However, some ransomware attempts to delete shadow copies before encrypting data.

Because of this, shadow copies should not replace properly secured and tested backups.

## BitLocker and TPM

BitLocker provides full-disk encryption for Windows devices.

Encryption helps protect data if a laptop or hard drive is lost, stolen, or discarded improperly.

The Trusted Platform Module, or TPM, helps securely protect encryption keys and supports device security.

Together, BitLocker and TPM help prevent unauthorized access to data stored on a physical device.

## System Performance and Monitoring

Windows includes tools that allow users and analysts to review:

- Running processes
- CPU usage
- Memory usage
- Disk activity
- Network activity
- Services

High resource usage does not automatically mean a system is compromised, but unusual activity can provide useful evidence during an investigation.

For example, an unknown process using a large amount of CPU or network bandwidth may need additional review.

## Windows Firewall Profiles

Windows Firewall uses three profiles depending on the type of network connection.

### Domain

The Domain profile applies when a device can authenticate to an organization’s domain controller.

### Private

The Private profile is generally used on trusted networks, such as a home network.

### Public

The Public profile is used on untrusted networks, such as public Wi-Fi, and normally applies more restrictive rules.

Firewall rules can control traffic based on applications, ports, protocols, services, and IP addresses.

## SOC Relevance

These Windows features can provide useful information during security investigations.

A SOC analyst may review:

- User and administrator permissions
- UAC activity
- Boot and startup settings
- Running processes and services
- Patch status
- Disk encryption
- Firewall profiles and rules
- System and network activity

Understanding how a normal Windows endpoint is configured makes it easier to identify suspicious changes, weak security controls, or unauthorized activity.

## Key Takeaways

This module helped me understand how Windows security controls work together to protect an endpoint.

Updates reduce exposure to known vulnerabilities. UAC and permissions restrict unauthorized changes. BitLocker and TPM protect stored data. Firewall profiles reduce network exposure. Monitoring tools provide visibility into system behavior.

My next step is to continue building on this foundation through Active Directory and Windows security monitoring labs.
