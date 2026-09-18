# NETWORKWALKS-B083-WK2-Footprinting-Reconnaissance-Network-Scanning
🛡️ PENETRATION TESTING
FOOTPRINTING & NETWORK SCANNING


Program / Batch: B083 – Networkwalks

Week: 02

Date: 18-09-2026

# 📚 Modules Completed
W2-PM1 – Multiple Kali Linux Tools
W2-PM2- Google Hacking Database / Google Dorking
W2-PM3 — Maltego Domain & Email Reconnaissance
W2-PM4 — theHarvester OSINT
W2-PM5 – Zenmap Scanning
# 🎯 Target
Networkwalks — authorized educational target
My own local LAN network
available resources
# 🔐 Authorization
All activities were performed within the authorized scope of the practical exercise or on my own network.

# ⚠️ Liability Disclaimer
This report is created for educational and cybersecurity training purposes. All testing was performed only on authorized systems and my own local network.

The commands and techniques shown should only be used in environments where proper permission has been obtained. Unauthorized scanning or access may violate laws and organizational policies.

# 📝 Introduction
During Week 02 of my Cybersecurity & Ethical Hacking internship, I worked on two important penetration-testing phases: footprinting/reconnaissance and network scanning.

For the first activity, I used several Kali Linux tools to collect publicly available information about the assigned domain. For the second activity, I used Zenmap to discover active devices on my own local network.

The main goal was to understand how cybersecurity professionals gather information about a target and document their findings before performing deeper security testing. 🔍

# 1-W2-PM1 – Multiple Kali Linux Tools
# 1 ### 🔹 WHOIS

WHOIS is used to retrieve publicly available domain registration information.

#### Command

```bash
whois networkwalks.com
```

<img width="1600" height="780" alt="image" src="https://github.com/user-attachments/assets/d56ac364-f12a-4542-a465-844f50dc5039" />

# 2 ### 🔹 WhatWeb

WhatWeb is a web reconnaissance tool used to identify technologies and software used by a website.

#### Command

```bash
whatweb networkwalks.com
```
<img width="1600" height="780" alt="image" src="https://github.com/user-attachments/assets/8d00df3e-584d-4479-a827-0d2a97d6ce1f" />

### 🔹 NSLookup

NSLookup is a DNS query tool used to retrieve DNS information about a domain or IP address.

#### Commands

```bash
nslookup example.com
nslookup -type=A example.com
nslookup -type=MX example.com
nslookup -type=NS example.com
```
| Command                | Finds                         |
| ---------------------- | ----------------------------- |
| `nslookup example.com` | Basic DNS information         |
| `-type=A`              | 🌐 IPv4 address               |
| `-type=MX`             | 📧 Mail servers               |
| `-type=NS`             | 🌍 Authoritative name servers |

<img width="1600" height="780" alt="image" src="https://github.com/user-attachments/assets/52d8f4f9-5064-4a31-a753-aa8f34d52782" />


### 🔹 curl -I

`curl -I` is used to retrieve the HTTP response headers of a website without downloading its page content.

#### Command

```bash
curl -I https://example.com
```
<img width="1600" height="780" alt="image" src="https://github.com/user-attachments/assets/faae1047-0325-4e12-aa2e-46856767c382" />

### 🔹 Wafw00f

Wafw00f is a web reconnaissance tool used to detect Web Application Firewalls (WAFs) protecting a website.

#### Command

```bash
wafw00f https://example.com
```
<img width="1600" height="780" alt="image" src="https://github.com/user-attachments/assets/1c291758-8424-4aed-b75b-96852cc2b610" />

### 🔹 DNSRecon

DNSRecon is a DNS reconnaissance tool used to collect DNS records and discover DNS-related information about a domain.

#### Command

```bash
dnsrecon -d example.com
```
<img width="1600" height="780" alt="image" src="https://github.com/user-attachments/assets/5e555d3e-ecb3-4ab1-97b1-9c2f13c74c6f" />






