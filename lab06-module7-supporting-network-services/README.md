# Lab 07 – Network Services and Troubleshooting

## Objective

The objective of this lab was to apply networking concepts by testing and observing common network services, protocols, ports, DNS records, HTTPS/TLS communication, time synchronization, active connections, wireless networking information, and troubleshooting indicators using command-line tools in macOS.

## Associated Notes

🔗 **Module 7 Notes:**
https://github.com/eduardo-durigon/comptia-a-plus-notes/blob/main/A%2B%20Core%201/Module-07/notes.md

These notes cover the networking concepts applied throughout this lab, including DNS resolution, network services, HTTP/HTTPS communication, TLS certificates, common ports, mail-related DNS records, NTP, traceroute analysis, and troubleshooting methodologies.

---

## Tools Used

* macOS Terminal
* ifconfig
* route
* scutil
* dig
* nslookup
* curl
* openssl
* netcat (nc)
* traceroute
* netstat
* lsof
* sntp
* system_profiler

---

## Tasks Completed

* Reviewed local IP address, default gateway, and DNS configuration
* Tested DNS name resolution
* Compared HTTP and HTTPS responses
* Inspected TLS certificate information
* Tested common network service ports
* Queried mail-related DNS records
* Verified network time synchronization
* Traced network paths to external destinations
* Reviewed active network connections and listening services
* Examined web server and CDN response headers
* Checked for APIPA/self-assigned addressing
* Reviewed wireless adapter and Wi-Fi capabilities

---

## Key Findings

### DNS Resolution

DNS successfully resolved multiple domain names into IP addresses, confirming that name resolution was functioning correctly.

### HTTP and HTTPS

HTTP and HTTPS both returned successful responses. HTTPS uses TLS encryption to protect data in transit, while HTTP transmits data without encryption.

### TLS Certificates

The TLS certificate inspection confirmed that GitHub presented a valid certificate issued by a trusted Certificate Authority, allowing secure encrypted communication.

### Port Connectivity

Common service ports including HTTP (80), HTTPS (443), and SSH (22) were reachable, demonstrating successful network connectivity to external services.

### Mail-Related DNS Records

MX records identified Google's mail servers, while TXT records contained verification and SPF information used to support email security and domain validation.

### Time Synchronization

Network Time Protocol (NTP) services were operational, ensuring accurate system time for logging, authentication, troubleshooting, and security purposes.

### Network Path Analysis

Traceroute successfully displayed multiple hops between the local system and remote destinations, demonstrating how traffic traverses ISP and backbone networks.

### Active Connections

Netstat and lsof identified active network connections, listening services, and established sessions, illustrating how endpoint systems communicate across networks.

### Web Infrastructure Analysis

HTTP response headers revealed information about content delivery networks, security controls, caching behaviour, redirects, and server configurations.

### DHCP and APIPA Verification

The system possessed a valid DHCP-assigned address and did not display a 169.254.x.x APIPA address, indicating normal network configuration.

### Wireless Networking

Wireless adapter information including supported PHY standards, channels, firmware versions, and wireless capabilities was reviewed using system_profiler. The legacy airport utility was unavailable on the installed macOS version.

---

## Screenshots

| Screenshot                          | Description                              |
| ----------------------------------- | ---------------------------------------- |
| 02-ip-gateway-dns-configuration.png | IP, gateway, and DNS configuration       |
| 03-dns-resolution-tests.png         | DNS resolution tests                     |
| 04-http-https-header-test.png       | HTTP and HTTPS header inspection         |
| 05-tls-certificate-inspection.png   | TLS certificate verification             |
| 06-common-port-testing.png          | Common service port testing              |
| 07-mail-dns-records.png             | Mail-related DNS records                 |
| 08-ntp-time-synchronization.png     | NTP time synchronization                 |
| 09-traceroute-network-path.png      | Network path tracing                     |
| 10-active-network-connections.png   | Active network connections using netstat |
| 11-web-proxy-cdn-response.png       | Web server and CDN response headers      |
| 12-limited-connectivity-check.png   | APIPA and DHCP verification              |
| 13-wireless-signal-information.png  | Wireless adapter information             |

---

## Reflection

This lab provided practical experience using networking and troubleshooting tools commonly used by IT support technicians, network administrators, and cybersecurity professionals.

The most valuable aspect of the lab was observing how network services can be tested directly from the command line. Tools such as dig, nslookup, curl, openssl, traceroute, netstat, lsof, and nc provided insight into DNS, routing, ports, encryption, connectivity, and system communication.

The lab reinforced the relationship between network services, protocols, ports, security controls, and troubleshooting methodologies. It also demonstrated how command-line tools can be used to investigate and validate network functionality in real-world environments.

Overall, this exercise strengthened practical networking skills that are directly applicable to future studies in CompTIA A+, Network+, Cisco networking, and cybersecurity.
