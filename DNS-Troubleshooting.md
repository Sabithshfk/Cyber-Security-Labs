# DNS Troubleshooting Guide

## What is DNS?

DNS (Domain Name System) translates domain names into IP addresses.

Example:
google.com → 142.250.x.x

## Common Symptoms

- Websites do not open by name.
- Websites may work using IP addresses.
- "DNS Server Not Responding" errors.

## Troubleshooting Steps

### 1. Check Internet Connectivity
- Verify network connection.
- Ping default gateway.

### 2. Test DNS Resolution
- Use:
  nslookup google.com

### 3. Ping Website by IP
- If IP works but name does not, DNS is likely the issue.

### 4. Flush DNS Cache
ipconfig /flushdns

### 5. Change DNS Server
- Test with:
  8.8.8.8
  1.1.1.1

### 6. Restart Network Adapter

### 7. Escalate if DNS infrastructure is unavailable

## Interview Answer

If a user cannot access websites, I would first verify internet connectivity and then test DNS resolution using nslookup. If websites work using IP addresses but not domain names, I would investigate DNS settings, flush the DNS cache, and test alternative DNS servers.
