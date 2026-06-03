## Network Troubleshooting

### 1. Internet Not Working
* **Check physical connections:** Verify all network cables are securely plugged in.
* **Inspect router lights:** Ensure the internet/WAN light is solid green or blinking.
* **Power cycle devices:** Unplug your modem and router for 30 seconds.
* **Test alternative devices:** Check if the issue affects one device or all.

### 2. DHCP Issues
* **Identify the symptom:** Device shows an "Unidentified Network" or "No IP Address" error.
* **Check IP assignment:** Run `ipconfig` (Windows) or `ifconfig` (Mac/Linux) to see your IP.
* **Spot APIPA addresses:** An IP starting with `169.254.x.x` means DHCP failed.
* **Renew your lease:** Run `ipconfig /renew` (Windows) or toggle Wi-Fi off and on.

### 3. DNS Issues
* **Identify the symptom:** You can ping IP addresses (like `8.8.8.8`) but cannot open websites.
* **Flush DNS cache:** Run `ipconfig /flushdns` in your command prompt.
* **Change DNS servers:** Switch to public DNS like Google (`8.8.8.8`) or Cloudflare (`1.1.1.1`).

### 4. Slow Internet Troubleshooting
* **Run a speed test:** Use an online tool to measure download and upload speeds.
* **Disconnect bandwidth hogs:** Disconnect cloud backups, torrents, or heavy streaming devices.
* **Switch to wired:** Use an Ethernet cable to rule out Wi-Fi interference.
* **Update network drivers:** Ensure your network adapter software is fully up to date.
