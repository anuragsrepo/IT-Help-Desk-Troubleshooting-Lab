# Ticket #004 — Storage Space / Unable to Save Files

---

## Ticket Information

- **Category:** Storage / Disk Space
- **Priority:** Medium
- **Status:** Resolved
- **Environment:** macOS
- **Type:** Simulated Help Desk Lab

---

## User Report

The user reports that they are experiencing storage-related issues and are unable to reliably save new files.

---

## Lab Scenario

A simulated storage environment was created to reproduce a common help desk scenario involving unnecessary files consuming disk space.

The test directory contained a work document, an old backup and a large cache file.

---

## Troubleshooting

### 1. Checked Available Disk Space

Disk usage was inspected using:

```bash
df -h /
```

This provided an overview of the filesystem's total, used and available storage.

---

### 2. Checked Directory Storage Usage

The total size of the simulated work directory was checked using:

```bash
du -sh /tmp/HelpDesk-Storage-Lab
```

The directory was consuming approximately **752 MB** of storage.

---

### 3. Identified Large Files

The contents were sorted by size using:

```bash
du -ah /tmp/HelpDesk-Storage-Lab | sort -hr
```

The investigation identified:

```text
502M  large-cache.dat
200M  old-backup.dat
50M   work-document.dat
```

The large cache file was identified as the largest unnecessary file.

---

### 4. Removed the Unnecessary Cache File

The unnecessary cache file was removed using:

```bash
rm /tmp/HelpDesk-Storage-Lab/large-cache.dat
```

The remaining files were then verified using:

```bash
ls -lh /tmp/HelpDesk-Storage-Lab
```

---

### 5. Verified Storage Recovery

Directory usage was checked again:

```bash
du -sh /tmp/HelpDesk-Storage-Lab
```

Storage usage decreased from approximately **752 MB to 250 MB**, confirming that approximately **502 MB** had been recovered.

---

### 6. Verified File Creation

A test file was created to confirm that files could be successfully saved:

```bash
echo "Save test successful" > /tmp/HelpDesk-Storage-Lab/save-test.txt
```

The file was then read using:

```bash
cat /tmp/HelpDesk-Storage-Lab/save-test.txt
```

Output:

```text
Save test successful
```

This confirmed successful file creation and access following the cleanup.

---

## Root Cause

An unnecessary large cache file was consuming a significant amount of storage within the simulated environment.

---

## Resolution

Identified the largest unnecessary file, removed the cache file and reduced the simulated directory's storage usage from approximately **752 MB to 250 MB**.

File creation was successfully tested after the cleanup to verify the resolution.

---

## Skills Demonstrated

- Storage troubleshooting
- macOS command-line diagnostics
- Disk usage analysis
- File and directory management
- `df`, `du`, `ls`, `sort` and `rm`
- Root cause analysis
- Incident documentation
- Resolution verification
