# Cybersecurity Homelab Portfolio

## Overview

This repository documents my cybersecurity homelab and security projects.

The lab was built using VMware on a Lenovo ThinkPad T14 and includes:

* pfSense Firewall/Router
* Windows Server 2022 Active Directory Domain Controller
* Windows 10 Pro Domain Workstation
* Kali Linux Attack Platform
* Metasploitable Vulnerable Target
* Sysmon Monitoring

## Virtual Machines

| System | Purpose |
|----------|----------|
| pfSense | Firewall / Router |
| DC1 | Active Directory Domain Controller |
| Windows 10 Pro | Domain Workstation |
| Kali Linux | Attack Platform |
| Metasploitable | Vulnerable Target |

## Network Architecture

```text
Internet
    │
    ▼
 pfSense
    │
    ▼
VMnet1 IP Host-Only
├── DC1 (Domain Controller)
├── Windows 10 Pro
├── Kali Linux
└── Metasploitable
```

## Objectives

* Learn Active Directory administration
* Practice network and system enumeration
* Develop detection and monitoring skills
* Simulate attacker techniques in a controlled environment
* Build practical cybersecurity experience

## Projects

1. Active Directory Deployment
2. SMB Enumeration Lab
3. Metasploitable Assessment
4. Sysmon Logging and Detection
5. BloodHound Active Directory Analysis
6. Security Onion Deployment (Planned)

