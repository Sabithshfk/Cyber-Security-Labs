# WiFi Troubleshooting

## Purpose

This guide covers common WiFi connectivity issues and troubleshooting steps used in IT Support environments.

---

## Common Symptoms

* Unable to connect to WiFi
* Connected but no internet access
* Slow internet speed
* Frequent disconnections
* Weak WiFi signal
* WiFi adapter not detected

---

## Initial Checks

### Verify WiFi is Enabled

Check whether WiFi is turned on:

* Windows Settings → Network & Internet → WiFi
* Verify Airplane Mode is disabled

---

### Check Signal Strength

Verify the device has sufficient signal.

Poor signal may be caused by:

* Distance from router
* Walls and obstacles
* Interference from other devices

Recommended:

* Move closer to the router.
* Relocate the router to a central location if possible.

---

## Verify Router Status

Check:

* Router is powered on
* Internet/WAN light is active
* Other devices can connect successfully

If multiple devices are affected, the issue may be with the router or ISP.

---

## Restart Network Equipment

1. Restart the computer.
2. Restart the router.
3. Wait 2–3 minutes for the connection to stabilize.

---

## Check IP Configuration

Open Command Prompt:

```cmd
ipconfig
```

Verify:

* Device has a valid IP address
* Default Gateway is present
* DNS servers are assigned

---

## Renew IP Address

Open Command Prompt as Administrator:

```cmd
ipconfig /release
ipconfig /renew
```

---

## Test Connectivity

### Ping Router

```cmd
ping 192.168.1.1
```

### Ping Google DNS

```cmd
ping 8.8.8.8
```

### Test DNS Resolution

```cmd
ping google.com
```

Results:

* Ping to router fails → Local network issue
* Ping to 8.8.8.8 fails → Internet issue
* Ping to 8.8.8.8 works but google.com fails → DNS issue

---

## DNS Troubleshooting

Flush DNS cache:

```cmd
ipconfig /flushdns
```

Configure public DNS:

```text
Primary DNS: 8.8.8.8
Secondary DNS: 8.8.4.4
```

---

## Driver Verification

Open Device Manager.

Check:

* Wireless adapter appears correctly
* No warning icons
* Driver is up to date

Update or reinstall the adapter driver if necessary.

---

## USB WiFi Adapter Troubleshooting

Check:

* Adapter is firmly connected
* Test different USB ports
* Install latest driver
* Test adapter on another PC

---

## Speed Testing

Use:

https://www.speedtest.net

Check:

* Download speed
* Upload speed
* Latency

Compare results with ISP package.

---

## When to Recommend Ethernet

Consider Ethernet when:

* Signal is weak
* PC is stationary
* Large downloads are required
* Gaming or video conferencing is used frequently

Ethernet generally provides:

* Lower latency
* Higher stability
* Better performance

---

## Real-World Example

### Customer Issue

* Old Lenovo desktop
* USB WiFi adapter installed
* Slow internet connectivity

### Findings

* Router located inside another room
* Weak signal reaching PC
* Windows updates significantly outdated

### Resolution

* Recommended moving router to a more central location
* Signal strength improved
* Internet connectivity stabilized
* Continued Windows update process

---

## Prevention

* Place router centrally
* Keep drivers updated
* Restart router periodically
* Use Ethernet where possible
* Maintain updated Windows versions

---

## References

* Windows Network Diagnostics
* Microsoft Network Troubleshooting
* ISP Router Best Practices
