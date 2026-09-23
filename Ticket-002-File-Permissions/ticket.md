# Ticket #002 — File Permissions / Access Denied

## Ticket Information

- **Category:** File Permissions / Access Control
- **Priority:** Medium
- **Status:** Resolved
- **Environment:** macOS
- **Type:** Simulated Help Desk Lab

---

## User Report

The user reports that they are unable to access a required work document and receive a "Permission denied" error when attempting to open the file.

---

## Lab Scenario

A temporary test environment was created to simulate a file access issue caused by incorrectly configured permissions.

The document was initially accessible before its permissions were intentionally modified to reproduce the reported issue.

---

## Troubleshooting Process

### 1. Verified the File Was Initially Accessible

Created a test document and confirmed that the user could successfully read its contents.

```bash
cat /tmp/HelpDesk-Permissions-Lab/project-document.txt
