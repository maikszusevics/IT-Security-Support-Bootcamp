# Case Study: MGM Resorts Data Breaches

## Overview

This case study explores two significant data breaches at MGM Resorts International: a data leak in 2019 and a ransomware attack in 2023. Both incidents highlight evolving cybersecurity threats, such as social engineering, third-party risk, and ransomware-as-a-service (RaaS).

---

## Table of Contents

1. [Incident 1: 2019 Data Leak](#incident-1-2019-data-leak)
2. [Incident 2: 2023 ALPHV/BlackCat Ransomware Attack](#incident-2-2023-alphvblackcat-ransomware-attack)
3. [Common Attack Vectors](#common-attack-vectors)
4. [Operational Impact](#operational-impact)
5. [Response & Mitigation](#response--mitigation)
6. [Security Lessons Learned](#security-lessons-learned)
7. [Glossary of Terms](#glossary-of-terms)

---

## Incident 1: 2019 Data Leak

### Summary

- **Date Discovered**: February 2020 (Breach occurred in 2019)
- **Data Compromised**: 10.6M–142M guest records
- **Attack Vector**: Unauthorised access to a cloud server
- **Data Exposed**:  
  - Full names  
  - Phone numbers  
  - Email addresses  
  - Dates of birth  
  - Hotel stay details  

### Root Causes

- **Cloud Misconfiguration**: Publicly accessible AWS S3 bucket
- **Lack of Monitoring**: No alert on unauthorised access
- **Inadequate Access Control**: Guest information not properly protected or segmented

### Impact

- Personal data of guests including celebrities, government officials, and executives was leaked.
- The leaked data was later published on hacking forums, increasing identity theft risk.

---

## Incident 2: 2023 ALPHV/BlackCat Ransomware Attack

### Summary

- **Date**: September 2023  
- **Threat Actor**: ALPHV / BlackCat Ransomware-as-a-Service (RaaS) group  
- **Attack Vector**: Social engineering via LinkedIn + vishing (voice phishing)  

### Technical Details

- **Initial Access**: Impersonation of an IT helpdesk call to obtain credentials of an MGM employee
- **Privilege Escalation**: Used access to Okta and internal systems to move laterally
- **Payload**: Custom ransomware deployed to lock systems and exfiltrate data

### Timeline

- **Sept 10**: Systems go down across MGM resorts
- **Sept 11-15**: Disruptions affect hotels, casinos, ATMs, keycards, slot machines, and digital check-ins
- **Sept 16**: ALPHV publicly claims responsibility
- **Sept 20+**: Recovery continues with FBI involvement

### Operational Impact

- Slot machines frozen or unusable
- Keycard systems disabled, guests locked out
- Hotel reservations managed manually
- Financial and reputation loss estimated in the **tens of millions of USD**

---

## Common Attack Vectors

| Vector                     | Description                                    | Used In |
| -------------------------- | ---------------------------------------------- | ------- |
| **Cloud Misconfiguration** | Poor security controls on cloud infrastructure | 2019    |
| **Social Engineering**     | Manipulating staff into giving access          | 2023    |
| **Vishing**                | Voice-based phishing targeting IT helpdesk     | 2023    |
| **Credential Theft**       | Gaining user/password info via impersonation   | 2023    |
| **Lateral Movement**       | Expanding access after entry                   | 2023    |
| **Ransomware**             | Encrypting systems and demanding payment       | 2023    |


## Operational Impact

| Area                  | Effect                                                |
| --------------------- | ----------------------------------------------------- |
| **Customer Services** | Check-ins and reservations had to be handled manually |
| **Revenue**           | Casino and hotel operations severely disrupted        |
| **Security**          | Customer data and internal systems exposed            |
| **Brand Trust**       | Customers lost confidence in MGM’s digital systems    |
| **Litigation**        | Class-action lawsuits filed post-breach               |


## Response & Mitigation

### After 2019 Leak

- **Security Review**: MGM confirmed it had secured the vulnerable cloud server
- **Monitoring Upgrades**: Improved detection of cloud misconfigurations
- **Data Classification**: New data protection strategies implemented

### After 2023 Attack

- **Incident Response Team Activated**: Internal and FBI investigations launched
- **Containment**: Systems were gradually brought offline to stop the spread
- **Recovery**: Gradual restoration of operations and systems over two weeks
- **Hardening Authentication**: Strengthened MFA (Multi-Factor Authentication) policies
- **Okta Forensics**: Examined identity platform logs for evidence of compromise
- **Staff Training**: Increased awareness of helpdesk-related social engineering

## Security Lessons Learned

| Lesson                                     | Explanation                                                                      |
| ------------------------------------------ | -------------------------------------------------------------------------------- |
| **People Are the Weakest Link**            | Social engineering can bypass even well-secured systems                          |
| **Identity Providers Must Be Hardened**    | Okta and similar tools are prime targets                                         |
| **Cloud Security is Non-Negotiable**       | Misconfigurations must be detected and prevented automatically                   |
| **Supply Chain & RaaS Threats Are Rising** | BlackCat/ALPHV operates as a ransomware-as-a-service model, which scales attacks |
| **Disaster Recovery Plans Must Be Tested** | Manual fallback systems must be ready to go live                                 |

---

## Glossary of Terms

- **Ransomware**: Malware that encrypts files and demands payment for decryption.
- **Vishing**: Voice phishing,using phone calls to trick people into revealing sensitive info.
- **Cloud Misconfiguration**: Incorrect settings in cloud platforms that expose data or allow access.
- **Lateral Movement**: A technique used by attackers to move deeper into a network once inside.
- **Ransomware-as-a-Service (RaaS)**: A model where threat actors lease ransomware tools to affiliates.
- **Okta**: A cloud-based identity and access management (IAM) provider, often used for SSO (Single Sign-On).
- **Privilege Escalation**: Gaining higher access rights than originally authorised.
- **MFA (Multi-Factor Authentication)**: Security system requiring multiple forms of identity verification.
