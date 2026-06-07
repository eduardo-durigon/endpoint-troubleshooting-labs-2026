# Module 5 Lab – Network Discovery and Wi-Fi Analysis on macOS

## Objective

The objective of this lab was to explore core networking concepts using macOS networking tools. The lab focused on identifying network interfaces, IP addressing, MAC addresses, DNS configuration, default gateways, connectivity testing, Wi-Fi analysis, and local network discovery.

By completing this lab, I gained hands-on experience using Terminal commands and wireless diagnostic tools commonly used in IT support and network troubleshooting.

---

## Related Notes

📚 [CompTIA A+ Core 1 – Module 5 Notes](https://github.com/eduardo-durigon/comptia-a-plus-notes/tree/main/A%2B%20Core%201/Module-05)

## Tools Used

* macOS Terminal
* Wireless Diagnostics
* Wi-Fi Status Menu
* Google Internet Speed Test

### Commands Used

```bash
ifconfig
ifconfig en0
route -n get default
scutil --dns
ping -c 4 192.168.0.1
ping -c 4 google.com
traceroute google.com
arp -a
```

---

## Screenshots

### Figure 1 – IP Address and MAC Address

Displayed interface details for `en0`, including the assigned IPv4 address and physical MAC address.

### Figure 2 – Default Gateway

Identified the default gateway used to route traffic outside the local network.

### Figure 3 – DNS Server Configuration

Reviewed DNS server settings and confirmed name resolution services were configured.

### Figure 4 – Local Network Connectivity Test

Successfully pinged the default gateway to verify communication with the local router.

### Figure 5 – Internet Connectivity Test

Successfully pinged Google to verify Internet access and DNS name resolution.

### Figure 6 – Traceroute Analysis

Used traceroute to observe the path packets travel from the local network to Google's infrastructure.

### Figure 7 – Wi-Fi Information

Reviewed wireless connection details including channel, frequency band, security settings, signal strength, and PHY mode.

### Figure 8 – ARP Table

Examined the ARP table to view mappings between IP addresses and MAC addresses on the local network.

### Figure 9 – Internet Speed Test

Measured real-world Internet performance, including download speed, upload speed, and latency.

---

## Key Findings

* The active wireless interface was identified as `en0`.
* The system successfully obtained an IP address from the local network.
* The default gateway was configured correctly and reachable.
* DNS resolution was functioning normally.
* Local and Internet connectivity tests completed successfully with no packet loss.
* Traceroute demonstrated how traffic traverses multiple routers before reaching a destination.
* The wireless connection operated on the 5 GHz band using 802.11ac (Wi-Fi 5).
* ARP entries confirmed communication between devices on the local network.
* Internet speed testing showed a high-performance broadband connection.

---

## Skills Practiced

* Identifying network interfaces
* Finding IP and MAC addresses
* Locating default gateways
* Reviewing DNS configurations
* Testing network connectivity
* Using ping and traceroute
* Viewing ARP tables
* Analyzing Wi-Fi information
* Performing basic network troubleshooting
* Documenting technical findings

---

## Reflection

This lab helped me connect networking theory with real-world system administration and troubleshooting tasks. Instead of only studying concepts such as IP addressing, DNS, gateways, and wireless networking, I was able to view and analyze these configurations directly on my MacBook Air.

Using Terminal commands increased my confidence working with networking tools and interpreting network information. I also gained a better understanding of how devices communicate on a local network and how Internet traffic travels through multiple routers before reaching its destination.

The Wi-Fi analysis portion of the lab provided useful insight into wireless performance, signal quality, channel selection, and security settings. Overall, this lab strengthened my foundational networking knowledge and reinforced concepts that are important for CompTIA A+, Network+, and future IT support roles.
