# SMB Enumeration

## Objective

Perform SMB enumeration against a vulnerable target to identify accessible network shares and evaluate potential security risks.

## Environment

Attacker:

* Kali Linux

Target:

* Metasploitable 2

## Discovery

Used Nmap to identify SMB services:

* TCP 139
* TCP 445

## Enumeration

Command:

smbclient -L //<TARGET-IP> -N

Discovered Shares:

* print$
* tmp
* opt
* IPC$
* ADMIN$

## Findings

Anonymous access was permitted.

Successfully connected to the tmp share and verified write permissions.

Test file uploaded successfully to the share.

## Security Impact

Potential risks include:

* Unauthorized file uploads
* Malware staging
* Data exfiltration
* Persistence mechanisms

## Skills Demonstrated

* SMB Enumeration
* Service Discovery
* Network Reconnaissance
* Security Assessment
* Documentation

## Lessons Learned

Misconfigured file shares can provide attackers with unauthorized access to systems and sensitive resources. Proper permissions and monitoring are essential to reducing risk.
