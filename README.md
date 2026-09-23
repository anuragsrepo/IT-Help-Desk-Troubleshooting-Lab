# IT Help Desk Troubleshooting Lab

A hands-on IT support troubleshooting lab documenting simulated help desk incidents, diagnostic processes, root cause analysis and resolutions.

This repository demonstrates practical Level 1 IT support skills through realistic troubleshooting scenarios performed in a macOS environment.

---

## Skills Demonstrated

- IT help desk troubleshooting
- TCP/IP networking fundamentals
- DHCP and default gateway configuration
- DNS troubleshooting
- Network connectivity testing
- Command-line diagnostics
- Root cause analysis
- Technical documentation
- Incident resolution
- File permission troubleshooting
- Unix/macOS permission management
- User and ownership verification

---

## Tools & Technologies

- macOS Terminal
- ping
- nslookup
- networksetup
- TCP/IP
- DHCP
- DNS
- GitHub documentation
- chmod
- ls -l
- whoami

---

## Help Desk Tickets

### Ticket #001 — Network Connectivity / DNS Resolution

**Issue:** User reports that their MacBook is connected to Wi-Fi but websites cannot be accessed.

**Investigation:** Network configuration, default gateway connectivity, internet connectivity and DNS resolution were systematically tested.

**Root Cause:** Incorrect DNS configuration prevented domain names from resolving despite functional network connectivity.

**Resolution:** Corrected the DNS server configuration and verified successful name resolution.

➡️ [View Ticket #001](./Ticket-001-Network-Connectivity/ticket.md)


### Ticket #002 — File Permissions / Access Denied

**Issue:** User reports that they are unable to access a required work document and receive a "Permission denied" error.

**Investigation:** Verified the current user, inspected the file permissions and identified that all read, write and execute permissions had been removed.

**Root Cause:** The file permissions were incorrectly configured as `000`, preventing the user from reading the file.

**Resolution:** Restored appropriate file permissions using `chmod 644` and verified that the document could be successfully accessed.

➡️ [View Ticket #002](./Ticket-002-File-Permissions/ticket.md)

---

## Project Purpose

This lab was created to develop and demonstrate practical troubleshooting skills relevant to entry-level IT Support, Service Desk and Help Desk roles.

Each ticket documents the issue, troubleshooting methodology, diagnostic commands, root cause, resolution and supporting evidence.
