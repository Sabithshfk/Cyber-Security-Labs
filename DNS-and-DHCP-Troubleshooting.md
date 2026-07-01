# DNS and DHCP Troubleshooting

## Purpose

This guide explains how to troubleshoot common DNS (Domain Name System) and DHCP (Dynamic Host Configuration Protocol) issues in Windows environments.

---

# What is DNS?

DNS translates domain names into IP addresses.

Example:

```
www.google.com → 142.250.xxx.xxx
```

Without DNS, users would need to remember IP addresses instead of website names.

---

# What is DHCP?

DHCP automatically assigns:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

to devices joining the network.

---

# Common Symptoms

DNS Issues

- Websites do not open.
- "DNS Server Not Responding"
- Can ping IP addresses but not domain names.

DHCP Issues

- No IP address assigned.
- Limited connectivity.
- APIPA address (169.254.x.x).

---

# Initial Checks

Verify:

- Network cable connected
- WiFi connected
- Router functioning
- Correct network selected

---

# Check Current IP Configuration

Open Command Prompt:

```cmd
ipconfig
```

For detailed information:

```cmd
ipconfig /all
```

Verify:

- IPv4 Address
- Default Gateway
- DNS Servers
- DHCP Enabled

---

# Release and Renew IP Address

Release current IP:

```cmd
ipconfig /release
```

Renew IP:

```cmd
ipconfig /renew
```

---

# Flush DNS Cache

```cmd
ipconfig /flushdns
```

---

# Register DNS Again

```cmd
ipconfig /registerdns
```

---

# Test DNS Resolution

Ping Google:

```cmd
ping google.com
```

If this fails:

Ping Google's DNS server:

```cmd
ping 8.8.8.8
```

If 8.8.8.8 works but google.com does not:

DNS is likely the problem.

---

# Test Internet Connectivity

```cmd
tracert google.com
```

---

# Verify DNS Server

Common DNS Servers

Google

```
8.8.8.8
8.8.4.4
```

Cloudflare

```
1.1.1.1
1.0.0.1
```

---

# Check Adapter Status

Open:

Network Connections

Verify:

- Adapter Enabled
- Connected

Disable and re-enable if necessary.

---

# DHCP Troubleshooting

If no IP is assigned:

Check:

- DHCP Server running
- Router functioning
- Ethernet cable
- Switch Port

Restart:

- Computer
- Router
- Switch (if necessary)

---

# APIPA Address

Example:

```
169.254.x.x
```

Meaning:

Computer could not obtain an IP address from DHCP.

Possible causes:

- Router failure
- DHCP server unavailable
- Network cable disconnected

---

# Windows Network Reset

Settings

↓

Network & Internet

↓

Advanced Network Settings

↓

Network Reset

Restart computer afterwards.

---

# Real-World Example 1

Hotel Guest WiFi

Issue:

Guest unable to browse websites.

Findings:

Device connected successfully.

DNS resolution failed.

Resolution:

Renewed IP configuration and verified DNS settings.

---

# Real-World Example 2

Customer Home Visit

Issue:

Desktop unable to connect to WiFi.

Findings:

USB WiFi adapter functioning.

Router placed too far away causing weak signal.

Resolution:

Recommended relocating the Dialog router to a more central location.

WiFi connected successfully afterwards.

---

# Best Practices

- Keep router firmware updated.
- Use reliable DNS servers.
- Restart networking equipment when required.
- Document static IP addresses.
- Avoid duplicate IP assignments.

---

# References

- Microsoft DNS Documentation
- Microsoft DHCP Documentation
- Windows Networking Best Practices
