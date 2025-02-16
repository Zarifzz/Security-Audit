# Botium Toys Security Audit

## Table of Contents
1. [Introduction](#introduction)
2. [Scenario](#scenario)
3. [Audit Methodology](#audit-methodology)
4. [Controls Assessment](#control-assessment)
5. [Compliance Checklist](#compliance-checklist)
6. [Remediation](#remediation)
7. [Conclusion](#conclusion)

---

## Introduction <a name="introduction"></a>
This security audit was conducted for **Botium Toys**, as part of my cybersecurity portfolio. This audit follows **industry best practices and compliance checks** such as:

- **National Institute of Standards and Technology Cybersecurity Framework (NIST CSF)**
- **Payment Card Industry Data Security Standard (PCI DSS)**
- **General Data Protection Regulation (GDPR)**
- **System and Organization Controls (SOC 1 & 2)**

This case study presents a security audit of Botium Toys, conducted using the **NIST Cybersecurity Framework (CSF)**. The audit aimed to identify security gaps, assess risk exposure, and recommend actionable improvements.

### **Objectives**
- Assess Botium Toys' cybersecurity posture.
- Identify vulnerabilities in key security areas.
- Provide recommendations to mitigate security risks.

---

## Scenario <a name="scenario"></a>
Botium Toys is a growing business with an increasing online presence. The **IT department is under pressure** to support global customers while ensuring compliance with **security regulations** such as PCI DSS and GDPR. The **IT Manager initiated this audit** to address concerns about:

- Business continuity
- Regulatory compliance
- Risk management
- Cyber threat mitigation

The IT team aims to **align security practices with industry standards** while ensuring that IT resources are well-managed and secure.

---

## Audit Methodology <a name="audit-methodology"></a>
The audit was structured around the five core functions of NIST CSF:

| **Function** | **Purpose** |
|-------------|------|
| **Identify** | Understand assets, risks, and governance. |
| **Protect** | Implement safeguards against cyber threats. |
| **Detect** | Identify cybersecurity incidents in real time. |
| **Respond** | Establish processes for responding to threats. |
| **Recover** | Ensure business continuity after a security event.|

### **Assessment Approach**
The audit evaluates **Administrative, Technical, and Physical security controls** into what control type it is:

Control types include, but are not limited to:
- Preventative
- Corrective
- Detective
- Deterrent

In addition to these specifications the audit also evaluates which **NIST CSF function** each control falls into. 


---

## Controls Assessment <a name="control-assessment"></a>


### **Administrative Controls**
| Control Name         | Type         | Status          | Priority | NIST CSF Function | Comments |
|----------------------|-------------|----------------|----------|-------------------|----------|
| Least Privilege     | Preventative | Not Implemented | High     | **Protect (PR.AC-4)** - Manage access permissions and enforce least privilege. | All employees have access to customer data |
| Disaster Recovery Plans | Corrective | Not Implemented | High  | **Recover (RC.RP-1)** - Ensure recovery processes and disaster planning. | There are no disaster recovery plans in place |
| Password Policies   | Preventative | Not Implemented | High     | **Protect (PR.AC-1)** - Enforce password security measures. | Employee password requirements are minimal |
| Access Control Policies | Preventative | Not Implemented | High | **Protect (PR.AC-1, PR.AC-3)** - Manage user authentication and access. | No policies put in place |
| Separation of Duties | Preventative | Not Implemented | High  | **Protect (PR.AC-5)** - Restrict privileges based on job roles. | Company CEO currently runs day-to-day operations and manages the payroll, this increases possibility of fraud/access to critical data |
| Legacy System Monitoring | Detective | Implemented | N/A | **Detect (DE.CM-7)** - Identify security anomalies in outdated systems. | Systems are monitored and Maintined |
| Legacy System Patch Management | Corrective | Not Implemented | High | **Protect (PR.IP-12)** - Ensure security patches are applied when available. | Legacy systems are on old patches |
| Manual Security Audits for Legacy Systems | Detective | Not Implemented | High | **Identify (ID.RA-1, ID.RA-2)** - Assess risks and vulnerabilities in legacy environments. | There are no future Audits/Procedure policy in place for Legacy Systems |

### **Technical Controls**
| Control Name         | Type         | Status          | Priority | NIST CSF Function | Comments |
|----------------------|-------------|----------------|----------|-------------------|----------|
| Firewall            | Preventative | Implemented    | N/A      | **Protect (PR.PT-3)** - Secure network boundaries. | In place, but should be regularly reviewed and updated |
| Intrusion Detection System (IDS) | Detective | Not Implemented | High | **Detect (DE.CM-1, DE.CM-7)** - Monitor network activity and detect anomalies. | No IDS in place |
| Encryption          | Deterrent    | Not Implemented | High     | **Protect (PR.DS-1, PR.DS-2)** - Encrypt sensitive data at rest and in transit. | Encryption is not currently used |
| Backups            | Corrective   | Not Implemented | High     | **Recover (RC.RP-1, RC.RP-2)** - Ensure data restoration and continuity. | No Backups of critical data |
| Antivirus Software  | Corrective   | Implemented | N/A     | **Protect (PR.IP-12)** - Implement anti-malware solutions. | Implemented but must be regularly updated |
| Password Manager for Employees | Preventative | Not Implemented | Medium | **Protect (PR.AC-1)** - Secure password storage and management. | No Password management system in place |

### **Physical Controls**
| Control Name         | Type         | Status          | Priority | NIST CSF Function | Comments |
|----------------------|-------------|----------------|----------|-------------------|----------|
| CCTV Surveillance   | Preventative | Implemented | N/A     | **Detect (DE.AE-1, DE.AE-2)** - Enable physical security monitoring. | CCTV Surveillance works properly |
| Locks (Offices, Storefront, Warehouse) | Preventative | Implemented | N/A | **Protect (PR.AC-2)** - Restrict physical access to assets. | Lock in place and policies to lock and unlock are set |
| Fire Detection & Prevention | Detective | Implemented | N/A | **Protect (PR.IP-10)** - Prevent and detect environmental threats. | All  fire protection systems work and in place |

---

## Compliance Checklist <a name="compliance-checklist"></a>
Botium Toys must comply with the following regulations:

### **Payment Card Industry Data Security Standard (PCI DSS)**
| Yes/No | Best Practice | Explanation |
|--------|--------------|-------------|
| ❌ No | Only authorized users have access to customers’ credit card information. | All employees have access to the company’s internal data |
| ❌ No | Credit card information is accepted, processed, transmitted, and stored internally, in a secure environment. | No encryption in place for credit card information, and all employees currently have access to internal data, including customers’ credit card information |
| ❌ No | Implement data encryption procedures to better secure credit card transaction touchpoints and data. | No encryption in place to ensure the confidentiality of customers’ financial information |
| ❌ No | Adopt secure password management policies. | Password policies are nominal, and no password management system in place |

### **General Data Protection Regulation (GDPR)**
| Yes/No | Best Practice | Explanation |
|--------|--------------|-------------|
| ❌ No | E.U. customers’ data is kept private/secured. | No Encryption in place to ensure the confidentiality of customers’ financial information |
| ✅ Yes | There is a plan in place to notify E.U. customers within 72 hours if their data is compromised/there is a breach. | Policy/plan in place to notify E.U. customers within 72 hours of a data breach |
| ❌ No | Ensure data is properly classified and inventoried. | Current assets are inventoried/listed, but not classified |
| ✅ Yes | Enforce privacy policies, procedures, and processes to properly document and maintain data. | Privacy policies, procedures, and processes have been developed and enforced |

### **System and Organization Controls (SOC Type 1, SOC Type 2)**
| Yes/No | Best Practice | Explanation |
|--------|--------------|-------------|
| ❌ No | User access policies are established. | Controls of Least Privilege and Separation of Duties are not in place; all employees have access to internally stored data |
| ❌ No | Sensitive data (PII/SPII) is confidential/private. | Encryption is not used to better ensure the confidentiality of PII/SPII |
| ✅ Yes | Data integrity ensures the data is consistent, complete, accurate, and has been validated. | Data integrity is in place |
| ❌ No | Data is available to individuals authorized to access it. | All employees have access to internally stored data; No authorization in place |

---

## Remediation <a name="remediation"></a>

### Critical Findings (Immediate Action Required)

1. **Principle of Least Privilege & Separation of Duties:**  
   Controls need to be developed and implemented to enforce strict adherence to the Principle of Least Privilege and Separation of Duties to minimize risk and improve access control across the organization.

2. **Disaster Recovery Plans (DRP):**  
   A robust disaster recovery plan should be established to ensure business continuity in the event of an unforeseen disaster, such as a physical fire or cyberattack.

3. **Password, Access Control & Account Management Policies:**  
   Development and enforcement of comprehensive password, access control, and account management policies to ensure that user credentials are managed securely.

4. **Intrusion Detection System (IDS):**  
   An IDS should be deployed to monitor network traffic, detect potential intrusions, and mitigate risks effectively.

5. **Encryption Protocols:**  
   Encryption measures for sensitive information, both in-transit (secure website transactions) and at-rest (disk drives containing sensitive data), must be implemented to ensure data confidentiality.

6. **Backups:**  
   Regular and secure backups should be conducted to ensure data integrity and availability in the event of an incident.

7. **Password Management System:**  
   Implement a password management system to enhance the security and management of user credentials.

8. **Manual Monitoring for Legacy Systems:**  
   Legacy systems should continue to be monitored manually, ensuring any vulnerabilities are quickly identified and addressed.


### Policies to be Developed & Implemented

- **PCI DSS & GDPR Compliance:**  
   Policies and procedures must be created to meet the requirements of PCI DSS and GDPR, particularly given Botium Toys' expansion into international markets, including the European Union.

- **SOC1 and SOC2 Compliance:**  
   User access policies and data protection practices should be aligned with SOC1 and SOC2 standards to enhance security and ensure proper controls are in place.

### Additional Findings (Future Considerations)

- **Physical Security Enhancements:**  
   Once the critical findings are addressed, further physical security measures should be considered:
   - **Time-Controlled Safe** to protect high-value items.
   - **Adequate Lighting** in sensitive areas.
   - **Signage indicating Alarm Service Provider** in restricted areas to notify personnel of monitored zones.



---

## Conclusion <a name="conclusion"></a>

To ensure Botium Toys remains compliant with PCI DSS, GDPR, and SOC1/SOC2, it is essential to prioritize the critical findings outlined above. Addressing these issues promptly will secure customer data, strengthen internal controls, and protect against potential threats. 

The implementation of disaster recovery plans, IDS, AV software, and encryption will enhance data resilience, while physical security measures such as CCTV, locks, and fire detection systems will safeguard both digital and physical assets. 

By taking these necessary steps, Botium Toys will improve its overall security posture, mitigate risks, and ensure a secure environment for its growing operations.


