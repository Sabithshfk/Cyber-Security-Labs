# DNS Basics and Troubleshooting

## What is DNS?

DNS (Domain Name System) translates human-readable domain names into IP addresses.

Example:

google.com → 142.250.x.x

Without DNS, users would need to remember IP addresses instead of website names.

---

## Common DNS Problems

- Websites not loading
- Slow website access
- Name resolution failures
- Incorrect DNS records

---

## Troubleshooting Steps

### 1. Check Internet Connectivity

Test whether the device has internet access.

### 2. Ping an IP Address

Example:

ping 8.8.8.8

If successful, internet connectivity exists.

### 3. Test DNS Resolution

Example:

nslookup google.com

Verify DNS is returning an IP address.

### 4. Change DNS Server

Common DNS servers:

Google:
8.8.8.8
8.8.4.4

Cloudflare:
1.1.1.1
1.0.0.1

### 5. Flush DNS Cache

Command:

ipconfig /flushdns

---

## Interview Question

### What is DNS?

DNS stands for Domain Name System. It translates domain names into IP addresses so devices can locate websites and services on a network.

### How would you troubleshoot a DNS issue?

I would verify internet connectivity, test DNS resolution using nslookup, check DNS server settings, flush the DNS cache, and test again.
