# Metasploitable Assessment

## Objective

Perform a security assessment of a deliberately vulnerable Linux system using standard reconnaissance and enumeration techniques.

## Environment

### Attacker

* Kali Linux

### Target

* Metasploitable 2

## Methodology

The assessment followed a structured approach:

1. Host Discovery
2. Port Scanning
3. Service Enumeration
4. Share Enumeration
5. Remote Service Investigation
6. Findings Documentation

## Service Discovery

Performed an Nmap service and operating system scan:

```bash
nmap -sV -O 192.168.1.105
```

### Key Findings

| Port | Service    | Version       |
| ---- | ---------- | ------------- |
| 21   | FTP        | vsftpd 2.3.4  |
| 22   | SSH        | OpenSSH 4.7   |
| 23   | Telnet     | Linux telnetd |
| 80   | HTTP       | Apache 2.2.8  |
| 139  | SMB        | Samba         |
| 445  | SMB        | Samba         |
| 1524 | Bind Shell | Root Shell    |
| 3306 | MySQL      | 5.0.51        |
| 5432 | PostgreSQL | 8.3           |
| 6667 | IRC        | UnrealIRCd    |
| 8180 | Tomcat     | Apache Tomcat |

## SMB Enumeration

Performed anonymous SMB enumeration:

```bash
smbclient -L //192.168.1.105 -N
```

Discovered shares:

* print$
* tmp
* opt
* IPC$
* ADMIN$

### Share Access

Successfully connected to the tmp share anonymously:

```bash
smbclient //(metasploitable IP)/tmp -N
```

Verified write permissions by uploading a test file.

### Security Impact

Anonymous write access to a network share could allow:

* Malware staging
* Data exfiltration
* Unauthorized file storage
* Persistence mechanisms

## FTP Enumeration

Connected to the FTP service anonymously:

```bash
ftp (metasploitable IP)
```

Anonymous authentication was permitted.

The FTP service appeared to be restricted to a jailed directory with limited access to the underlying filesystem.

### Security Impact

Anonymous FTP access may expose sensitive files or provide attackers with an additional access path if improperly configured.

## Remote Shell Discovery

Discovered a bind shell service listening on TCP port 1524.

Connected using:

```bash
nc (metasploitable IP) 1524
```

Successfully obtained a remote root shell:

```bash
root@metasploitable:/#
```

### Security Impact

This represents a complete system compromise without authentication and would be considered a critical vulnerability in a production environment.

## Skills Demonstrated

* Network Reconnaissance
* Service Enumeration
* SMB Enumeration
* FTP Enumeration
* Linux System Investigation
* Security Documentation
* Risk Assessment

## Lessons Learned

This assessment demonstrated the importance of proper service hardening, access control, and continuous monitoring. Even basic enumeration techniques can reveal significant attack surface and critical security weaknesses.

## Future Work

* Web Application Assessment
* Tomcat Enumeration
* Database Enumeration
* Detection Development
* Log Analysis using Sysmon and Chainsaw

## Screenshots

Include:

* Nmap Service Scan
* SMB Enumeration Results
* Anonymous FTP Login
* Bind Shell Access
* Metasploitable Network Configuration
