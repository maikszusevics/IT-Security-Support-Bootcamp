# Case Study: Ransomware Attacks on the NHS

## Overview

This case study examines major ransomware incidents that have impacted the UK’s National Health Service (NHS), with a detailed focus on the 2017 WannaCry attack and the 2024 Qilin/Synnovis incident. The document analyzes causes, impacts, response strategies, and lessons learned, while explaining relevant technical terms.

---

## Table of Contents

1. [Incident 1: WannaCry Ransomware (2017)](#incident-1-wannacry-ransomware-2017)
2. [Incident 2: Qilin Ransomware via Synnovis (2024)](#incident-2-qilin-ransomware-via-synnovis-2024)
3. [Common Threat Vectors](#common-threat-vectors)
4. [Operational Impact](#operational-impact)
5. [Response & Mitigation](#response--mitigation)
6. [Security Lessons Learned](#security-lessons-learned)
7. [Glossary of Terms](#glossary-of-terms)

---

## Incident 1: WannaCry Ransomware (2017)

### Summary

- **Date**: 12 May 2017  
- **Type**: Ransomware Worm  
- **Exploit Used**: EternalBlue (SMBv1 vulnerability)  
- **Ransom Note**: Demanded Bitcoin  
- **Infection Method**: No user interaction; wormable spread over networks  

### Technical Details

- **Vulnerability Used**: MS17-010 (patched by Microsoft in March 2017)
- **Operating Systems Affected**: Windows XP, Windows 7, Server 2003, others
- **Propagation**: Exploited Server Message Block (SMBv1) protocol for lateral movement
- **Payload Behavior**: Encrypted files with ".WNCRY" extension and displayed ransom note

### NHS Impact

- **Affected**: Over 80 NHS Trusts, 603 primary care organizations
- **Consequences**:
  - Canceled 19,000 appointments
  - Shut down A&E (Accident & Emergency) services
  - Disabled diagnostic equipment (e.g., MRI scanners)
  - Blocked access to electronic health records (EHRs)

### Root Causes

- Unsupported and unpatched legacy systems (e.g., Windows XP)
- Poor segmentation in internal networks
- No offline or immutable backups for quick recovery
- Inadequate monitoring and intrusion detection

## Incident 2: Qilin Ransomware via Synnovis (2024)

### Summary

- **Date**: May 2024  
- **Threat Actor**: Qilin ransomware group (Russia-based)  
- **Target**: Synnovis , pathology service provider for NHS Trusts  
- **Type**: Targeted ransomware + data exfiltration

### Technical Details

- **Vector**: Supply chain compromise (attack on a third-party NHS partner)
- **Impact**:
  - Lab systems encrypted
  - Patient and lab test data possibly exfiltrated
  - Trusts affected: Guy’s and St Thomas’, King’s College Hospital

### Operational Consequences

- Delays in blood tests and diagnostics
- Surgery postponements due to unavailable pathology results
- Emergency labs redirected to other facilities, increasing strain

---

## Common Threat Vectors

| Vector | Description | NHS Impact |
|--------|-------------|------------|
| **Phishing Emails** | Emails containing malicious attachments or links that trigger malware download | Common entry point for targeted ransomware |
| **Remote Desktop Protocol (RDP)** | Attackers brute-force or use stolen credentials to gain system access | Growing issue with exposed endpoints |
| **Unpatched Vulnerabilities** | Attackers exploit known flaws in outdated software | Key cause in WannaCry |
| **Lateral Movement** | Malware moves across internal networks once inside | Enabled broad infection in WannaCry |
| **Supply Chain Attack** | Third-party service providers are compromised to reach target networks | Seen in Synnovis/Qilin case |


## Operational Impact

| Area | Effect |
|------|--------|
| **Clinical Services** | Appointments and procedures canceled or delayed |
| **Patient Safety** | Risk increased due to inaccessible records or test results |
| **Staff Workflow** | Manual processes adopted, increasing workload |
| **Public Trust** | Confidence in NHS IT systems undermined |
| **Financial Loss** | Estimated £92m (WannaCry: £19m for lost services + £73m for recovery and upgrades) |


## Response & Mitigation

### After WannaCry (2017–2021)

- **Patch Management Overhaul**: Introduction of automated updates and monitoring
- **Device Upgrades**: Migrated to Windows 10 from unsupported OSes
- **Central Alerting**: NHS Digital's CareCERT issued real-time security bulletins
- **Investment**: £150m allocated to cybersecurity improvements
- **Awareness Training**: Programs deployed across Trusts to reduce phishing susceptibility

### Post-2020 Developments

- **Zero Trust Architecture** pilots to restrict access based on verification
- **Network Segmentation** to isolate clinical systems from administration networks
- **Third-Party Vetting**: Stronger contracts and audits for vendors
- **Immutable Backups**: Offline and tamper-resistant backup solutions introduced
- **Endpoint Protection**: Rollout of EDR (Endpoint Detection and Response) systems

## Security Lessons Learned

| Lesson | Explanation |
|--------|-------------|
| **Legacy System Risks** | Unsupported OS increases vulnerability to exploits |
| **Patch Management is Critical** | Timely updates are essential to close known vulnerabilities |
| **Segmentation Saves Systems** | Limiting internal access reduces ransomware spread |
| **Supplier Risk is Your Risk** | Vendors must meet your security standards |
| **Training is Ongoing** | Human error is a key vector; training must be continuous |
| **Backups Need Protection** | Backups should be offline, encrypted, and regularly tested |

---

## Glossary of Terms

- **Ransomware**: Malware that encrypts data and demands payment for decryption.
- **SMB (Server Message Block)**: A protocol for sharing files and printers on networks; SMBv1 had serious security flaws.
- **EternalBlue**: An exploit developed by the NSA and leaked by the Shadow Brokers, used in WannaCry.
- **Phishing**: Social engineering method that tricks users into opening malware or revealing credentials.
- **Zero Trust Architecture**: A model where no device or user is trusted by default, even inside the network.
- **Lateral Movement**: Tactic used by attackers to move across a network after an initial breach.
- **Immutable Backup**: A backup that cannot be modified or deleted by ransomware or unauthorized users.
- **EDR (Endpoint Detection and Response)**: A security solution that monitors and reacts to threats on end-user devices.

# Case Study 2: Data Breach and MGM

