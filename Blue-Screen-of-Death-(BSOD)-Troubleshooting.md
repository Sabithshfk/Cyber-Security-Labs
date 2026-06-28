# Blue Screen of Death (BSOD) Troubleshooting

## Purpose

This guide explains how to diagnose and troubleshoot Windows Blue Screen of Death (BSOD) errors.

---

# What is a BSOD?

A Blue Screen of Death (BSOD) is a critical Windows system error that causes the operating system to stop to prevent hardware or software damage.

---

# Common Symptoms

- Blue screen appears unexpectedly
- Automatic restart
- Boot loop
- System freezes before restart
- Error code displayed

---

# Common Causes

- Faulty RAM
- Corrupted drivers
- Windows update issues
- Overheating
- SSD/HDD failure
- Corrupted system files
- BIOS issues
- Failing power supply

---

# Initial Checks

Ask the user:

- When did the issue start?
- Did any hardware change recently?
- Were drivers updated?
- Was Windows updated recently?

---

# Safe Mode

If Windows cannot boot normally:

1. Interrupt boot three times.
2. Open Advanced Startup.
3. Select:

Troubleshoot

↓

Advanced Options

↓

Startup Settings

↓

Safe Mode

---

# Check Event Viewer

Open:

```cmd
eventvwr.msc
```

Review:

Windows Logs

↓

System

Look for:

- Critical
- Error
- BugCheck events

---

# Check Reliability Monitor

Run:

```cmd
perfmon /rel
```

Review application crashes and hardware failures.

---

# Check System Files

Run:

```cmd
sfc /scannow
```

Then:

```cmd
DISM /Online /Cleanup-Image /RestoreHealth
```

Restart the computer.

---

# Memory Diagnostics

Run:

```cmd
mdsched.exe
```

Restart and allow Windows Memory Diagnostic to complete.

If errors are found:

- Test RAM individually.
- Replace faulty module.

---

# Disk Health

Run:

```cmd
chkdsk C: /f /r
```

Restart when prompted.

---

# Driver Verification

Open:

Device Manager

Check:

- Unknown devices
- Warning symbols
- Recently installed drivers

Update or roll back problematic drivers.

---

# Windows Updates

Install pending updates.

If issue started after update:

Settings

↓

Windows Update

↓

Update History

↓

Uninstall Updates

---

# Temperature Check

Monitor CPU temperature.

Possible tools:

- HWMonitor
- HWiNFO

High temperatures may indicate:

- Dust buildup
- Failed cooling fan
- Poor thermal paste

---

# BIOS

If hardware was upgraded:

- Verify BIOS settings.
- Update BIOS only if recommended by manufacturer.

---

# Common BSOD Codes

Examples:

- CRITICAL_PROCESS_DIED
- MEMORY_MANAGEMENT
- IRQL_NOT_LESS_OR_EQUAL
- PAGE_FAULT_IN_NONPAGED_AREA
- SYSTEM_SERVICE_EXCEPTION

---

# Preventive Maintenance

- Keep Windows updated.
- Install official drivers.
- Maintain proper cooling.
- Scan for malware.
- Test RAM when instability appears.

---

# Real-World Learning

Although no major BSOD case has been encountered yet, the troubleshooting methodology follows:

- Gather information
- Check hardware
- Check Windows integrity
- Verify drivers
- Review logs
- Test memory
- Test storage
- Isolate root cause

---

# References

- Microsoft Windows Documentation
- Microsoft Bug Check Reference
