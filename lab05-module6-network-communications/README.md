# Module 06 - Network Troubleshooting Lab (macOS)

## Objective

The objective of this lab was to practice network troubleshooting techniques using built-in macOS tools. The lab focused on identifying network configuration settings, verifying connectivity, testing DNS resolution, analyzing routing paths, and validating service availability through common TCP ports.

---

## Tools Used

* macOS Terminal
* Wi-Fi TCP/IP Settings
* `ipconfig`
* `route`
* `scutil`
* `ping`
* `nslookup`
* `traceroute`
* `nc` (Netcat)

---

## Commands Used

```bash
ipconfig getifaddr en0

route -n get default

scutil --dns

ping -c 4 192.168.0.1

ping -c 4 8.8.8.8

nslookup google.com

traceroute google.com

nc -vz google.com 443

nc -vz example.com 80
```

---

## Results Summary

| Test                           | Result  |
| ------------------------------ | ------- |
| IP Address Verification        | Success |
| Default Gateway Identification | Success |
| DNS Configuration Review       | Success |
| Gateway Ping Test              | Success |
| Internet Connectivity Test     | Success |
| DNS Resolution Test            | Success |
| Traceroute Analysis            | Success |
| Port 443 Connectivity Test     | Success |
| Port 80 Connectivity Test      | Success |
| DHCP Lease Review              | Success |

---

## Key Takeaways

* Identified and verified local IP addressing information.
* Located the default gateway and understood its role in routing traffic.
* Examined DNS server configuration and verified DNS functionality.
* Tested local and internet connectivity using ICMP.
* Used traceroute to visualize the path packets take across multiple networks.
* Verified application-layer service availability using Netcat.
* Reviewed DHCP configuration and lease renewal settings within macOS.
* Practiced a structured troubleshooting methodology commonly used in IT support environments.
