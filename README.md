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



## 🔹 W2-PM3 – Maltego Domain & Email Reconnaissance

### What is Maltego?

Maltego is an OSINT and reconnaissance tool used to collect publicly available information and visualize relationships between different entities.

### Key Concepts

- **Entity** – An object such as a domain, IP address, email address, or person.
- **Transform** – An operation used to discover related information.
- **Graph** – A visual representation of relationships between entities.

### Objective

To perform authorized domain and email reconnaissance and understand how publicly available information can be connected and visualized.

### Target

Only authorized educational targets and publicly available information were used.

<img width="1920" height="1080" alt="Screenshot 2026-09-19 093928" src="https://github.com/user-attachments/assets/342eaac3-5627-4389-962e-af90bdd2e0bb" />


## 🔎 W2-PM2 – Google Hacking Database (GHDB)

### Objective

To understand Google Hacking Database (GHDB) and learn how search operators can be used during authorized reconnaissance to identify publicly indexed information.

### Tool Used

- Google Hacking Database (GHDB)
- Google Search

### Activity

I explored GHDB and examined a Google dork entry related to publicly indexed webcam interfaces.

### Example Dork

```text
intitle:"webcamXP" inurl:8080
```

### What the operators mean

- `intitle:` → searches for pages containing specific text in the page title.
- `inurl:` → searches for pages containing specific text in the URL.
- `"webcamXP"` → searches for the exact phrase.

### Screenshots

#### 1. GHDB Search

<img width="1885" height="917" alt="Screenshot 2026-09-19 095635" src="https://github.com/user-attachments/assets/03ff476d-dd90-4d17-911f-e893e6a85e04" />


#### 2. GHDB Dork Details

<img width="1913" height="961" alt="Screenshot 2026-09-19 095719" src="https://github.com/user-attachments/assets/529e2391-ab17-41aa-83f5-b52091e41dd0" />

<img width="1620" height="893" alt="Screenshot 2026-09-19 095559" src="https://github.com/user-attachments/assets/663af3b4-fa13-44db-97c7-9a8a46cf71bd" />


### ⚠️ Authorization & Safety

This activity was performed for educational reconnaissance purposes. Google dorks should only be used to identify information within an authorized scope. Discovering an exposed system does not grant permission to access, monitor, or interact with it.

No unauthorized system was accessed or tested.

## 🔎 W2-PM4 – theHarvester OSINT

### Objective

To use theHarvester for collecting publicly available information about an authorized domain during the OSINT reconnaissance phase.

### Tool Used

- theHarvester
  <img width="1600" height="780" alt="WhatsApp Image 2026-09-19 at 1 53 00 PM" src="https://github.com/user-attachments/assets/2fe23b0b-9e42-46b8-8846-928e92141d83" />


### Command

```bash
theHarvester -d example.com -b bing
```

### Information Collected

Depending on the available public sources, theHarvester can identify:

- Email addresses
- Subdomains and hostnames
- IP addresses
- URLs
- Other publicly available domain-related information

### 🔹 Commands Used

#### 1. Baidu Search

```bash
theHarvester -d microsoft.com -l 1000 -b baidu
```

- `-d` → specifies the target domain
- `-l` → limits the number of results
- `-b` → specifies the data source
<img width="1600" height="780" alt="image" src="https://github.com/user-attachments/assets/7a132e45-de96-4d53-8344-15cc837cf03d" />


#### 2. Multiple Sources

```bash
theHarvester -d microsoft.com -l 50 -b all
```

- `-d` → specifies the target domain
- `-l` → limits the results to 50
- `-b all` → uses all supported sources
<img width="1600" height="780" alt="image" src="https://github.com/user-attachments/assets/0175453c-557b-4fbb-a58f-6726e407b241" />













### Purpose

The purpose of this activity was to understand how publicly available information can be collected and used during the reconnaissance phase of a penetration test.

### ⚠️ Authorization

Only authorized educational targets and publicly available information were used. Sensitive information was not intentionally collected or published.


## 🔎 W2-PM5 – Zenmap Scanning

### Objective

To understand network discovery and scanning using Zenmap, the graphical interface for Nmap.

### Tool Used

- Zenmap
- Nmap

### Target

My own authorized lab network.

### Network Information

```text
IP Address: 10.0.0.4
Netmask: 255.255.255.0
Broadcast: 10.0.0.255
```
<img width="1600" height="780" alt="WhatsApp Image 2026-09-19 at 2 05 47 PM" src="https://github.com/user-attachments/assets/d0ed0c24-6ff3-44b1-9de0-0daaf615144e" />

<img width="1600" height="780" alt="WhatsApp Image 2026-09-19 at 2 05 39 PM" src="https://github.com/user-attachments/assets/3228169b-f358-487c-b87f-1a81f4e270ab" />
<img width="1600" height="780" alt="WhatsApp Image 2026-09-19 at 2 05 43 PM" src="https://github.com/user-attachments/assets/891781c3-47a6-4033-b2d4-037244c012e2" />
<img width="1600" height="780" alt="WhatsApp Image 2026-09-19 at 2 05 47 PM (1)" src="https://github.com/user-attachments/assets/0c522bfe-b0d4-48d9-a82b-d49a9426dcc4" />


## 🗂 Report 

---

<a id="s1"></a>
## `[ SECTION 01 ]` Authorization & Liability Disclaimer

This assessment was performed only against systems and assets for which written authorization was obtained — specifically **networkwalks.com** , **my own Home Lab** — and/or systems and devices that I own myself.

All activities described in this report are conducted for authorized security assessment, education and research purposes only. Nothing in this document should be used to access, scan or test any system without explicit written permission from its owner. Every action taken is the responsibility of the person performing it. Misuse of these techniques may result in criminal charges, civil liability, loss of employment and a permanent record. In most jurisdictions, unauthorized access to a computer system is a crime even when no damage occurs.


---

<a id="s2"></a>
## `[ SECTION 02 ]` Executive Summary


An authorized security assessment was conducted against the lab environment using Maltego, Zenmap/Nmap, and Nessus to evaluate OSINT exposure, identify active network hosts, and assess system vulnerabilities.

The Maltego OSINT assessment identified one publicly discoverable organizational email address, info@networkwalks.com. As this is a generic mailbox and no credentials or sensitive information were identified, the finding presents a Low risk, with its primary value being reconnaissance and potential exposure to phishing or spam.

Using Zenmap, five active devices were identified within the authorized lab network: Kali Linux, Windows 7, Windows Server 2016, Windows 10, and the VirtualBox NAT Network gateway. Since the scan was limited to host discovery, these results represent network reconnaissance information rather than vulnerabilities.

The Nessus scan produced a significantly larger set of findings on the Windows 7, Windows Server 2016, and Windows 10 systems. The results indicate issues including missing security updates, outdated components, and potentially insecure configurations, with the legacy Windows 7 system requiring particular attention.

Overall, the assessment found that the main security exposure lies within the Windows systems identified by Nessus, rather than the OSINT or network-discovery findings. Remediation should focus on prioritizing high-severity vulnerabilities, applying security updates, reviewing configurations, and isolating or replacing unsupported legacy systems where appropriate.

---

<a id="s3"></a>
## `[ SECTION 03 ]` Scope & Objectives

**Objectives**
- ▸ Map the external OSINT footprint of the authorized target using Maltego
- ▸ Discover and map live hosts, services and topology on the in-scope network using Zenmap
- ▸ Scan and analyze vulnerabilities of the discovered network endpoints using Nessus

**In Scope**

networkwalks.com
10.0.0.0/24 NatNetwork
HOMELAB domain of Windows Server 2016

**Out of Scope**

Web Applications
Web Servers
Other Networks (WAN, Internet)

**Constraints / Rules of Engagement**
> 
Only allowed to scan email domains under explicit authorization from networkwalks.com
Home network reconnaissance is limited under an isolated Virtual Box NatNetwork
No exploitation allowed; only passive reconnaissance and vulnerability/risk analysis permitted. 
---

<a id="s4"></a>
## `[ SECTION 04 ]` Methodology & Tools Used

The table below lists each tool used during this engagement and its purpose.

| Tool | Purpose |
|---|---|
| **Maltego** | Graph-based OSINT reconnaissance — mapping domains, subdomains, infrastructure, email addresses, personas and related entities tied to the target. |
| **Zenmap (Nmap GUI)** | Active network discovery and mapping — identifying live hosts, IP/MAC addresses, open ports, services and network topology. |
| **Nessus** | Passive network reconnaissance, vulnerability assessment, and analysis |
| **Supporting OS** | Kali Linux and Windows 11 |
| **Target OS** | Windows 7, Windows Server 2016, Windows 10 |


---

<a id="s5"></a>
## `[ SECTION 05 ]` Activities Performed

### 5.1 OSINT Reconnaissance (Maltego)

- ▸ Domain: networkwalks.com
- ▸ Infrastructure mapped: 1 email mapping
- ▸ Email addresses: 1 email address (info@networkwalks.com)
- ▸ Notable relationships or pivot points surfaced by the graph: Contact point email mapped to networkwalks.com

### 5.2 Network Mapping (Zenmap)

- ▸ Subnet / range scanned: 10.0.0.0/24
- ▸ Live hosts identified: 5
- ▸ Notable open ports / services: 80, 135, 3389, 445
- ▸ Topology exported (Yes/No, format): Yes, ".pdf"

### 5.3 Vulnerability Assessment (Nessus)
- ▸ Hosts scanned: 10.0.0.10, 10.0.0.16, 10.0.0.7
- ▸ Live hosts identified: 3
- ▸ Situation: All 3 hosts need serious risk assessment and mitigation
- ▸ Considerations: Legacy isolation, patching, responsible server configuration
---

<a id="s6"></a>
## `[ SECTION 06 ]` Findings & Risk Analysis

Based on the OSINT reconnaissance, network mapping activities, and vulnerability assessment, the following potential risks were identified.

## 🔒 Maltego Risk Assessment — networkwalks.com

**Scope:** networkwalks.com

| # | Finding | Evidence / Observation | Potential Impact | Risk |
|---|---|---|---|---|
| 1 | **Email Identified** | maltego email transform returned an email address of "info@networkwalks.com" and the email ID exposes itself to networkwalks.com | Potential for exposure to phishing and spam. | 🟢 **Low** |

**Risk level key:** 🔴 Critical &nbsp;&nbsp; 🟠 High &nbsp;&nbsp; 🟡 Medium &nbsp;&nbsp; 🟢 Low

## 🔒 Network Risk Assessment — Homelab Domain (10.0.0.0/24)

**Scope:** 4 live remote VMs and 1 hypervisor | DC (Win Server, 2016), Win10 workstation, Win7/2008R2 legacy host, unidentified gateway/hypervisor, unclassified host.

| # | Finding | Evidence / Observation | Potential Impact | Risk |
|---|---|---|---|---|
| 1 | **Domain Controller fully exposed** | `10.0.0.16` (DC01) has LDAP(389/3268), Kerberos(88), SMB(445), NetBIOS(139), RPC(135/593), WinRM(5985) all open to the whole /24. FQDN `homelab.local` disclosed. | A compromised host anywhere on this network has direct line-of-sight to AD for enumeration, Kerberoasting, and SMB relay/attack against the DC — the single point of failure for the domain. | 🔴 **Critical** |
| 2 | **Unsupported / legacy OS in domain** | `10.0.0.7` fingerprints as **Windows 7 / Server 2008 R2** (96% confidence) — both long past end-of-life with no vendor patches. | No security updates means any newly disclosed SMB/RPC vuln (e.g., EternalBlue-class) is permanently exploitable; a soft entry point for lateral movement to the DC. | 🔴 **Critical** |
| 3 | **RDP + database exposed on gateway/hypervisor host** | `10.0.0.1` exposes **RDP (3389)**, **PostgreSQL (5432)**, VMware auth (902/912), and IIS (80) simultaneously — an unusual, high-value multi-service host. | RDP is a top brute-force/ransomware entry vector; an internet- or LAN-reachable DB with no visible auth context risks direct data exposure or use as a pivot into the virtualization layer. | 🟠 **High** |
| 4 | **Minimal patch/version visibility across endpoints** | `10.0.0.7` and `10.0.0.10` return only port 135 (RPC) with no service banners; DC's `microsoft-ds` reports as **Server 2008 R2–2012 build strings** despite guessed OS being 2016 — inconsistent SMB stack. | Blind spots prevent confirming patch level; mismatched SMB version strings suggest outdated or unpatched components that standard vuln scanning would need to verify directly. | 🟡 **Medium** |

---
**Risk level key:** 🔴 Critical &nbsp;&nbsp; 🟠 High &nbsp;&nbsp; 🟡 Medium &nbsp;&nbsp; 🟢 Low

## 🔒 Nessus Risk Assessment — Homelab Domain (10.0.0.0/24)

**Scope:** 3 live remote VMs and 1 hypervisor| DC (Win Server, 2016), Win10 workstation, Win7/2008R2 legacy host, gateway/hypervisor.

| # | Finding | Evidence / Observation | Potential Impact | Risk |
|---|---|---|---|---|
| 1 | **Vulnerability in TCP/IP** | The TCP/IP stack in use on the remote Windows 7 host is affected by an integer overflow vulnerability. | Sending a continuous flow of specially crafted UDP packets to a closed port can result in arbitrary code execution in kernel mode. | 🔴 **Critical** |
| 2 | **DNS Server RCE** | A remote code execution (RCE) vulnerability exists in Windows Domain Name System servers (Server 2016) when they fail to properly handle requests. | An attacker who successfully exploited the vulnerability could run arbitrary code in the context of the Local System Account. | 🔴 **Critical** |
| 3 | **SMBv1 Improper Handling** | An information disclosure vulnerability (in Server 2016) exists in Microsoft Server Message Block 1.0 (SMBv1) due to improper handling of certain requests. | An unauthenticated, remote attacker can exploit this, via a specially crafted packet, to disclose sensitive information. (For instance, the Eternal Blue exploit leverages this vulnerability for unauthorized access.  | 🔴 **Critical** |
| 4 | **Missing Crucial Patch** | The remote Windows 10 host is missing security update to latest patch of Oct 2025. It is, therefore, affected by multiple vulnerabilities | The system is vulnerable to various issues involving buffer overflow and secure boot misconfigurations which can be exploited by attacker for denial of service and malicious execution.| 🟠 **High** |
| 5 | **IIS Path Disclosure** | The NAT Network gateway (10.0.0.1), corresponding to the VirtualBox host machine, reveals the physical path of the host's IIS webroot when a nonexistent page is requested. | Detailed error messages are useful for debugging but should not be exposed to remote clients, as they can reveal internal filesystem of core Host Machine information (in this case, my own PC) and assist further reconnaissance or exploitation. | 🟡 **Medium** |

**Risk level key:** 🔴 Critical &nbsp;&nbsp; 🟠 High &nbsp;&nbsp; 🟡 Medium &nbsp;&nbsp; 🟢 Low

***These findings are observations from reconnaissance, mapping, and scanning activities, not confirmed exploitable vulnerabilities. No exploitation was performed as part of this engagement unless explicitly stated above. Further authorized pentesting would be required to confirm actual exploitability.***

---

<a id="s7"></a>
## `[ SECTION 07 ]` Recommendations

### `Maltego Risks`
1. **Review the public OSINT footprint** — Periodically audit what Maltego / public sources reveal about the domain networkwalks.com.
2. **Reduce infrastructure exposure** — Based on the audit and periodic scanning, decide what infrastructure needs less exposure than required by implementing least privilege principle.

---

### `Discovery Risks`
| # | Finding Addressed | Recommendation | Why This Approach (Preserves Availability) |
|---|---|---|---|
| 1 | DC fully exposed on flat network | Place `10.0.0.16` behind host-based firewall rules restricting 389/445/3268/5985 to authorized admin subnets only. Leave 88 (Kerberos)/389 (LDAP) reachable from client subnet — domain auth must keep working. | Blocks lateral-movement/enumeration paths from workstations without breaking domain logon, DNS, or GPO — AD stays fully functional for legitimate clients. |
| 2 | Windows 7 / Server 2008 R2 host (`10.0.0.7`) | Short-term: isolate on its own VLAN with only the specific ports/services it needs to talk to (no general LAN access). Medium-term: schedule replacement/upgrade — this OS cannot be secured long-term. | Isolation removes it as a pivot point immediately without shutting it down, keeping whatever workload it runs online while you plan the actual decommission. |
| 3 | RDP + PostgreSQL exposed on `10.0.0.1` | Restrict RDP (3389) and PostgreSQL (5432) to a defined admin IP allow-list or jump host; keep IIS (80) open only if it's a required service. Enable MFA on RDP if not already. | Admins retain full remote access and DB connectivity from their own machines; only unrestricted/anonymous LAN exposure is removed — zero disruption to legitimate admin workflow. |
| 4 | Unclear patch level / inconsistent SMB versions | Run an authenticated vulnerability scan (e.g., Nessus/OpenVAS credentialed scan) against DC and both workstations to confirm actual patch state before deciding on fixes. | Read-only verification step — no config changes, no downtime risk — but removes guesswork before touching production SMB/AD services. |

---

### `Nessus Risks`
| # | Finding Addressed | Recommendation |
|---|---|---|
| 1 | **Vulnerability in TCP/IP**  | Microsoft has released a set of patches for Windows Vista, 2008, 7, and 2008 R2. Apply the relevant patch update for short term use. However, isolation and upgrade to latest Windows OS is the long term recommended approach.|
| 2 | **DNS Server RCE** | Apply the appropriate security update or mitigation as described in the Microsoft advisory. |
| 3 | **SMBv1 Improper Handling** | Apply the applicable security update for your Windows version, in this case, Windows Server 2016: KB4019472|
| 4 | **Missing Crucial Patch** | Apply security update to October Patch 2025 (Windows 10 22H2): 5066791 |
| 5 | **IIS Path Disclosure** | Configure IIS (C:\Windows\System32\inetsrv\) to disable Detailed Errors for remote clients and use generic/custom error pages. Also review the application under C:\inetpub\wwwroot to ensure errors do not disclose local file paths. |

---

<a id="s8"></a>
## `[ SECTION 08 ]` Conclusion

This engagement combined OSINT reconnaissance (Maltego), active network mapping (Zenmap/Nmap), and credentialed vulnerability assessment (Nessus) against the networkwalks.com homelab. OSINT exposure was minimal (a single contact email). Network mapping identified 5 hosts — including a Windows Server 2016 DC, a Windows 10 workstation, and a legacy Windows 7 host — with RDP, SMB, LDAP, Kerberos, and a database exposed on a flat, unsegmented network. Nessus confirmed these exposures as real, exploitable vulnerabilities: a kernel-level TCP/IP flaw on Windows 7, DNS Server RCE and SMBv1 disclosure on the DC, missing patches on Windows 10, and IIS path disclosure on the gateway.

Overall, the security posture is **weak to moderate**: the Domain Controller and legacy endpoints are directly reachable and unpatched, placing the core of the domain at meaningful risk. The key takeaway is that each phase validated the next — OSINT mapped the external footprint, network scanning revealed the internal attack surface, and vulnerability scanning proved that surface maps to real, exploitable risk. Network segmentation, patching, and least-privilege exposure are the priority fixes.

All activity in this report was performed strictly within the scope authorized by networkwalks.com. No exploitation was conducted; confirming exploitability would require a separately 
## `[ SECTION 9]` EVIDENS
<img width="1600" height="780" alt="image" src="https://github.com/user-attachments/assets/4f3bc13b-daf5-478c-b328-d9a1e24821a1" />
<img width="1600" height="780" alt="image" src="https://github.com/user-attachments/assets/7c983cd3-1d8f-4d95-b6db-0a7cb9c45a7d" />
<img width="1600" height="780" alt="image" src="https://github.com/user-attachments/assets/e0337c05-2b35-46ff-898a-2fe207c1ea01" />
<img width="1600" height="780" alt="image" src="https://github.com/user-attachments/assets/b692c519-f5b7-4a6d-a0fa-671ee6cd3e48" />
<img width="1600" height="780" alt="image" src="https://github.com/user-attachments/assets/96be2862-f233-4b2d-bf22-7f69d7b497ce" />
<img width="1600" height="780" alt="image" src="https://github.com/user-attachments/assets/dc71dc6c-e4ae-4acf-84b2-b36ba0d14afc" />



---

<a id="s10"></a>
## `[ SECTION 10 ]` Author & Project Information

**👤 Author**
`Md Nazeerullaa` — `NETWORKWALKS`
LinkedIn: `linkedin.com/in/md-nazeerullaa-51211133a`

**📌 Project Information**
Program: `W2-PM3-FINAL` | Week / Phase: `[2]`










