# Internet-Troubleshooting.md

This document provides step-by-step procedures for diagnosing and resolving network connectivity issues.

## 1. Single User No Internet
* **Isolate device:** Check if other devices on the same network can access the internet.
* **Verify hardware:** Ensure the network cable is secure or Wi-Fi is connected.
* **Reboot device:** Restart the computer to clear stuck network stacks.
* **IP check:** Run `ipconfig` (Windows) or `ifconfig` (Mac/Linux) to verify IP assignment.

## 2. Multiple Users No Internet
* **Check infrastructure:** Inspect switches, routers, and access points for power and error lights.
* **ISP outage:** Verify the status line or contact the Internet Service Provider.
* **Core gateway:** Ping the default gateway to check internal routing health.

## 3. DNS Issues
* **Symptoms:** Can ping public IP addresses (like `8.8.8.8`) but cannot load websites via domain names.
* **Test resolution:** Run `nslookup google.com` to check if names resolve.
* **Flush cache:** Execute `ipconfig /flushdns` to clear corrupt DNS data.
* **Alternative DNS:** Temporarily switch device DNS settings to `8.8.8.8` or `1.1.1.1` for testing.

## 4. DHCP Issues
* **Symptoms:** Device has an APIPA address starting with `169.254.x.x`.
* **Release/Renew:** Run `ipconfig /release` followed by `ipconfig /renew`.
* **Scope check:** Verify the DHCP server has available IP addresses left in its pool.

## 5. Cable/Wi-Fi Checks
* **Physical cables:** Swap out suspected bad Ethernet cables with tested replacements.
* **Wi-Fi signal:** Check RSSI levels and potential physical interference sources.
* **SSID verification:** Ensure the user is connected to the correct corporate or guest network.

## 6. Ping Testing
* **Loopback:** Ping `127.0.0.1` to test the local network card functionality.
* **Gateway:** Ping the local router IP to test local network connectivity.
* **External:** Ping `8.8.8.8` to test connection outside the local network.

## 7. Escalation Process
* **Document findings:** Collect the affected usernames, MAC addresses, and ping test results.
* **Ticket creation:** Log a high-priority ticket in the IT service portal.
* **Contact NetOps:** Page the Network Operations team if a widespread outage is confirmed.
