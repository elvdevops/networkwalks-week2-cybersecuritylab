# NetworkWalks — Week 2 Cybersecurity Project

## Footprinting with Kali Tools & Network Scanning with Zenmap

</div>

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ver-Virtualbox%20v7.2-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Linux-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Penetration%20Testing-C00000?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Virtualization-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Kali%20Linux-404040?style=flat-square&labelColor=C00000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Waqas%20Karim%20CCIE-C00000?style=flat-square" />
</p>

This repository contains my **Week 2 hands-on cybersecurity exercises** completed as part of my Cybersecurity and Ethical Hacking training with **NetworkWalks**.

The project focuses on two fundamental areas of cybersecurity reconnaissance:

1. **Footprinting with Kali Tools** — gathering and analyzing information about authorized targets using passive and low-impact reconnaissance techniques.
2. **Network Scanning with Zenmap** — discovering and analyzing active hosts within an authorized network.

The goal was to develop practical experience with reconnaissance, network discovery, information gathering, and security assessment documentation.

---

## Project Objectives

The main objectives of this project were to:

* Understand the reconnaissance phase of a security assessment.
* Perform authorized domain and web footprinting.
* Gather publicly available information about target infrastructure.
* Identify web technologies and DNS information.
* Analyze HTTP response headers.
* Identify potential Web Application Firewalls.
* Discover active hosts within an authorized LAN.
* Identify IP addresses and available MAC address information.
* Visualize discovered network infrastructure.
* Document security assessment activities and findings.

---

# 1. Footprinting with Kali Tools

The first section of the project focuses on **information gathering and footprinting using Kali Linux**.

Several reconnaissance tools were used to examine different aspects of authorized targets.

### Tools Used

| Tool         | Purpose                                       |
| ------------ | --------------------------------------------- |
| **WHOIS**    | Domain registration and ownership information |
| **WhatWeb**  | Web technology identification                 |
| **NSLookup** | DNS and domain-to-IP resolution               |
| **cURL**     | HTTP response and header analysis             |
| **WAFW00F**  | Web Application Firewall detection            |
| **DNSRecon** | DNS record enumeration                        |

### Activities Performed

#### WHOIS

Used to retrieve publicly available domain registration information.

```bash
whois networkwalks.com
```

#### WhatWeb

Used to identify technologies exposed by the target web application.

```bash
whatweb networkwalks.com
```

#### NSLookup

Used to investigate DNS resolution and DNS records.

```bash
nslookup networkwalks.com
```

#### cURL

Used to inspect HTTP response headers.

```bash
curl -I https://networkwalks.com
```

#### WAFW00F

Used to determine whether a recognizable Web Application Firewall was protecting the target.

```bash
wafw00f https://networkwalks.com
```

#### DNSRecon

Used for additional DNS enumeration.

```bash
dnsrecon -d networkwalks.com
```

### Documentation

The detailed footprinting report is available in:

`README.md`

Raw command outputs and screenshots are also included as supporting evidence.

---

# 2. Network Scanning with Zenmap

The second section focuses on **network discovery and scanning using Zenmap/Nmap**.

The exercise was performed against an authorized network to identify active hosts and understand the structure of the local network.

### Activities Performed

* Identified the local IP address.
* Identified the subnet and default gateway.
* Discovered live hosts.
* Recorded discovered IP addresses.
* Examined MAC address information where available.
* Reviewed host details.
* Generated a network topology visualization.
* Documented the scan results.

### Example Host Discovery Command

```bash
nmap -sn 10.0.0.0/24
```


> The example above is for demonstration only. The actual scan was performed against an authorized network.

### Documentation

The detailed network scanning report is available in:

`network-scanning-with-zenmap/README.md`

Supporting scan results, screenshots, and the topology PDF are included in the project directory.

---

# Project Structure

```text
networkwalks-week2-cybersecurity-project/
│
├── README.md
│
├── footprinting-with-kali-tools/
│   ├── 
│   ├── whois.txt
│   ├── whatweb.txt
│   ├── nslookup.txt
│   ├── curl-headers.txt
│   ├── wafw00f.txt
│   ├── dnsrecon.txt
│   └── screenshots/
│       ├── whois.png
│       ├── whatweb.png
│       ├── nslookup.png
│       ├── curl-headers.png
│       ├── wafw00f.png
│       └── dnsrecon.png
│
└── network-scanning-with-zenmap/
    ├── module5-report-zenmap-network-scanning.docx
    ├── docs/
        ├── topology.pdf
    └── screenshots/
        ├── zenmap-installation.png
        ├── local-ip.png
        ├── live-hosts.png
        ├── host-details.png
        └── topology.png
```

---

# Key Learning Outcomes

This project provided hands-on experience with several important cybersecurity concepts.

### Reconnaissance

I learned how different tools can be combined to build an understanding of a target's externally visible infrastructure.

### DNS Enumeration

I gained practical experience identifying DNS information and understanding how domain names relate to network infrastructure.

### Web Reconnaissance

I practiced identifying technologies, HTTP response information, and defensive technologies exposed by web applications.

### Network Discovery

I learned how host discovery can be used to identify active systems within an authorized network.

### Network Topology

Using Zenmap, I gained experience visualizing discovered systems and developing a high-level understanding of network structure.

### Security Documentation

The project also reinforced the importance of recording:

* Commands used
* Tool output
* Screenshots
* Observations
* Network information
* Assessment scope
* Authorization

---

# Security and Ethical Considerations

Reconnaissance and network scanning can expose information about organizations, applications, and connected devices.

For this reason, all activities documented in this repository were performed within an **authorized security-testing scope**.

I obtained permission from the relevant target/network owners before carrying out reconnaissance and scanning activities against the target networks used in these exercises.

The activities were conducted for **authorized cybersecurity training, assessment, and educational purposes**.

Sensitive information such as internal IP addresses, MAC addresses, hostnames, credentials, private data, or other identifying information should be appropriately redacted before public distribution.

---

# Disclaimer

> **I obtained permission from the relevant target and network owners before carrying out reconnaissance and network scanning activities documented in this project.**

All techniques demonstrated in this repository were performed against authorized targets or networks for cybersecurity training and educational purposes.

This repository is intended to demonstrate responsible security testing and should **not** be interpreted as permission to scan or assess systems belonging to third parties.

Unauthorized reconnaissance, scanning, enumeration, or security testing may violate organizational policies and applicable laws.

Always obtain appropriate authorization and clearly define the scope of an assessment before testing a system or network.

---

# Conclusion

The **NetworkWalks Week 2 Cybersecurity Project** provided practical experience with two important stages of a security assessment: **footprinting and network discovery**.

By using Kali Linux reconnaissance tools and Zenmap/Nmap, I was able to practice gathering information about authorized targets, identifying network resources, documenting findings, and visualizing network infrastructure.

This project builds a foundation for progressing into more advanced areas of ethical hacking, including:

* Enumeration
* Vulnerability assessment
* Web application security testing
* Network security testing
* Exploitation in controlled environments
* Security monitoring
* DevSecOps and cloud security

---

## Author

**Elvis Halim**

Cybersecurity | Ethical Hacking | DevSecOps | Cloud Infrastructure

GitHub: `github.com/elvdevops`

---

**NetworkWalks Cybersecurity Training — Week 2**
