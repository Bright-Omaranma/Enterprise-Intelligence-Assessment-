# Enterprise Intelligence Assessment

## Open-Source Exposure and Security Intelligence (OSINT)

### Primary Subject of Assessment
**National Institute of Information Technology, Port Harcourt (NIITPH)**

---

### Report Information

| Item | Details |
|------|---------|
| **Prepared By** | Bright Madubuochi Omaranma |
| **Classification** | Confidential – For Academic and Internal Review Use Only |
| **Date** | 10 July 2026 |

---
## 📑 Table of Contents

- [Introduction](#-introduction)
- [Overview](#-overview)
- [Objectives](#-objectives)
- [Scope](#-scope)
- [Tools Used](#-tools-used)
- [Methodology](#-methodology)
- [Findings](#-findings)
- [Intelligence Correlation](#-intelligence-correlation)
- [Intelligence Assessment](#-intelligence-assessment)
- [Risk Analysis](#-risk-analysis)
- [Recommendations](#-recommendations)
- [References](#-references)

---
## Introduction 
This report presents the results of an Enterprise Threat Intelligence Assessment conducted using Open-Source Intelligence (OSINT) techniques and limited network reconnaissance. The objective was to identify publicly available information that could increase the organization's exposure to cyber threats and evaluate potential security risks from an external threat actor's perspective. The assessment used only publicly accessible information and non-intrusive reconnaissance. No unauthorized access or exploitation was performed.

## Overview 
Threat intelligence supports the identification and analysis of publicly available information that could be leveraged by adversaries. This assessment evaluates externally observable information using passive OSINT techniques and limited infrastructure reconnaissance.

## Objective 
-	To identify publicly available information
-	Access employee and organizational exposure 
-	Discover digital assets and footprints 
-	Investigate publicly available infrastructure
-	Correlate intelligence findings into meaningful findings 
-	Access security risks based on collected intelligence
-	Produce a professional intelligence report

## Scope
This assessment was limited to passive open-source intelligence activities using publicly available information. No intrusive or unauthorized activities was performed.

## Tools Used

| Tool | Purpose |
|------|---------|
| Google Dorking | Advanced search for publicly available information using specialized search operators |
| WHOIS | Domain registration information and ownership details |
| theHarvester | Email address, subdomain, and hostname discovery |
| Wayback Machine | Historical website analysis and retrieval of previous website versions |
| Maltego | Relationship mapping and link analysis between entities |
| HTTrack | Offline website analysis through website mirroring |
| Shodan | Discovery of internet-facing devices, services, and exposed infrastructure |
| OSINT Framework | Collection of OSINT resources for domain and intelligence gathering |
| GanttProject | Project planning, scheduling, and task management |

**Table 1 — Tools referenced in the OSINT assessment and their stated purposes.**

## Methodology

This assessment followed the **Intelligence Cycle methodology** to ensure a structured, repeatable, and effective intelligence-gathering process.

### Intelligence Cycle Phases

| Phase | Description |
|-------|-------------|
| **Planning** | Defined the assessment objectives, scope, targets, and intelligence requirements. |
| **Collection** | Gathered publicly available information using OSINT tools and reconnaissance techniques. |
| **Processing** | Organized, filtered, and prepared collected data for analysis. |
| **Analysis** | Evaluated collected information to identify patterns, risks, vulnerabilities, and potential threats. |
| **Dissemination** | Presented findings, conclusions, and recommendations to relevant stakeholders. |

## Findings

The findings below consolidate all evidence and observations recorded in the assessment, organized according to the activities performed. Corresponding screenshots are provided in the **Evidence** column of each finding.

The **Risk Level** values are mapped to the relevant **MITRE ATT&CK® Reconnaissance (TA0043)** techniques rather than using subjective ratings such as High, Medium, or Low.

| **MITRE ATT&CK Technique** | **Technique Name** | **Description** |
|----------------------------|--------------------|-----------------|
| **T1589** | Gather Victim Identity Information | Collection of employee names, job roles, email addresses, and other identity-related information. |
| **T1590** | Gather Victim Network Information | Collection of IP addresses, network topology details, infrastructure relationships, and technical information about the target environment. |
| **T1593** | Search Open Websites/Domains | Discovery of publicly available information through search engines and open web sources. |
| **T1594** | Search Victim-Owned Websites | Targeted searches of organization-owned websites, including current and archived content, using techniques such as Google Dorking. |
| **T1595** | Active Scanning | Identification of hosts, services, open ports, and exposed infrastructure through scanning activities. |
| **T1596** | Search Open Technical Databases | Collection of technical information from public databases, including WHOIS records and DNS registration data. |

### Findings Summary

The assessment findings demonstrate how publicly available information can be collected and analyzed to identify organizational exposure, infrastructure details, and potential reconnaissance activities by threat actors.

# Findings

The findings below consolidate all evidence and observations recorded in the assessment, organized according to the activities performed. Corresponding screenshots are provided in the **Evidence** column of each finding.

The **Risk Level** values are mapped to the relevant **MITRE ATT&CK® Reconnaissance (TA0043)** techniques rather than subjective ratings such as High, Medium, or Low.

---

## A. Individual OSINT Case Study — Wigwe University Lecturer Profile

| Finding | Risk Level | Evidence |
|---------|------------|----------|
| A Google dork (`intitle:wigwe university`) was used to locate the official Wigwe University website (`www.wigweuniversity.edu.ng`) as the starting point for identifying a named lecturer's public profile. | T1593 — Search Open Websites/Domains | Fig. A1 — Google dork search results identifying the university's official website. |
| A review of the current Wigwe University website, including the College of Science and Computing section where the lecturer's details previously appeared, returned no profile information, indicating the profile has since been removed from the live site. | T1594 — Search Victim-Owned Websites | Fig. A2 — Current university website; lecturer profile no longer present. |
| Using the Wayback Machine, an archived snapshot dated 6 August 2025 was located and found to still contain the lecturer's profile, confirming previous affiliation despite removal from the current website. | T1594 — Search Victim-Owned Websites | Fig. A3 — Wayback Machine archived snapshot (6 Aug 2025) retaining the lecturer's profile. |

---

# B. NIITPH — Passive Reconnaissance (Exposure Identification)

| Finding | Risk Level | Evidence |
|---------|------------|----------|
| Dork query `site:niit.com "Port Harcourt"` was used for domain enumeration; results returned contact and organizational reference pages. | T1594 — Search Victim-Owned Websites | Fig. B1 — Domain enumeration dork results. |
| Dork query `"NIIT Port Harcourt" "@"` was used for email discovery; results returned email address patterns and contact addresses. | T1589 — Gather Victim Identity Information | Fig. B2 — Email discovery dork results. |
| Dork query `site:linkedin.com "NIIT Port Harcourt"` was used for employee profiling; results identified staff names and roles. | T1589 — Gather Victim Identity Information | Fig. B3 — LinkedIn employee-profiling dork results. |
| Dork query `site:niitph.com` was used for asset discovery; results returned indexed pages and possible entry points on the organization's web presence. | T1594 — Search Victim-Owned Websites | Fig. B4 — Indexed pages and entry points identified via site-restricted search. |

---

# C. NIITPH — Information Leakage

Passive reconnaissance using Google Dorking revealed information that could potentially assist attackers in targeting the institute or its clients.

### Identified Exposed Information

- Named senior employee (**Centre Head — Precious Ogulu Tom**) with direct email address:
  - `centrehead@niit-ph.com`

- Named senior employee (**Chief Counsellor**) with direct email address:
  - `ibigbareretoru@niitph.com`

- Organizational phone numbers identified:
  - `+234-915-311-0525`
  - `+2340-806-962-5113`
  - `08107076917`

- Public support email address:
  - `support@niitph.com`

- Accessible login portal:
  - `http://www.niitph.com/encore/auth`

**Analyst Observation:**  
The exposed information increases the organization's human attack surface and may enable spear-phishing campaigns, impersonation attempts, and targeted credential-harvesting attacks against exposed services.

| Finding | Risk Level | Evidence |
|---------|------------|----------|
| Employee identities, direct email addresses, phone numbers, support contacts, and login portal information were publicly discoverable. | T1589 — Gather Victim Identity Information | Fig. C1–C3 — Staff identity/contact details and support-email listing. |

---

# D. NIITPH — Infrastructure Intelligence (OSINT Framework & WHOIS)

| Finding | Risk Level | Evidence |
|---------|------------|----------|
| The official URL (`www.niitph.com`) was queried through OSINT Framework, which returned the website IP address: `185.53.179.146`. | T1590 — Gather Victim Network Information | Fig. D1 — OSINT Framework lookup result showing resolved IP address. |
| WHOIS analysis revealed domain registration information, including privacy-protected registrant details, confirmed location (`Rivers`, `NG`), creation date (May 2025), expiration date (May 2026), unsigned DNSSEC status, and shared hosting indicators from bgp.he.net. | T1596 — Search Open Technical Databases | Fig. D2 — WHOIS / bgp.he.net domain registration data. |

---

# E. NIITPH — Relationship Mapping (Maltego)

| Finding | Risk Level | Evidence |
|---------|------------|----------|
| The Maltego website entity was used to validate information gathered through Google Dorking and OSINT Framework while identifying additional infrastructure relationships through transforms. | T1590 — Gather Victim Network Information | Fig. E1–E3 — Maltego transform graphs for the niitph.com website entity. |

---

# F. NIITPH — Human Attack Surface

| Finding | Risk Level | Evidence |
|---------|------------|----------|
| Staff information collected from LinkedIn and the official website demonstrated identifiable employees who could potentially be targeted through social-engineering techniques. | T1589 — Gather Victim Identity Information | Fig. F1 — Staff information gathered from public platforms. |

---

# G. NIITPH — Infrastructure Accessibility

| Finding | Risk Level | Evidence |
|---------|------------|----------|
| Nmap was executed from Kali Linux against the identified IP address (`185.53.179.146`). Host discovery was performed using `nmap -sn -PE 185.53.179.146`, followed by full port scanning using `nmap -p- 185.53.179.146` to identify accessible services. | T1595 — Active Scanning | Fig. G1 — Nmap host-discovery and port-scan output. |

---

**Table 2 — Consolidated OSINT assessment findings mapped to MITRE ATT&CK® Reconnaissance techniques.**

## Intelligence Correlation

The assessment correlated multiple intelligence sources to identify organizational exposure and potential attack surfaces.

The following information was identified through OSINT activities:

- Public employee information** including names, roles, and organizational affiliations.
- Contact details** such as email addresses and publicly available phone numbers.
- Login portal URL** exposed through publicly accessible resources.
- Publicly visible infrastructure information** including domain details and IP address intelligence.
- Human attack surface** through identifiable employees who may be targeted using social-engineering techniques.
- Infrastructure visibility** through passive reconnaissance and relationship mapping.

Basic **Nmap reconnaissance** was documented as part of the assessment process; however, actual scan output results were not provided. Therefore, no conclusions were made regarding:

- Open ports
- Running services
- Service versions
- Potential vulnerabilities

The intelligence correlation indicates that publicly available information alone can provide sufficient insight into an organization's digital footprint and potential areas of exposure.

## Intelligence Assessment

The assessment identified that publicly available employee information may increase the organization's exposure to targeted cyber threats, including:

- **Phishing attacks** through personalized email campaigns.
- **Social engineering attempts** targeting identifiable employees.
- **Business Email Compromise (BEC)** through impersonation of trusted individuals.
- **Credential harvesting attempts** targeting exposed login portals or authentication services.

However, no evidence of:

- Successful compromise
- Unauthorized access
- Data breach
- Confirmed malicious activity

was provided during the assessment.

The findings represent potential exposure based on publicly available intelligence and do not confirm that an active attack has occurred.

## Risk Analysis

The assessment identified several exposure areas that may increase the organization's overall cyber risk, including:

- Employee information exposure** — Publicly available staff details may enable targeted phishing, social engineering, and impersonation attempts.
- Public contact information exposure** — Disclosed email addresses, phone numbers, and support contacts may increase the likelihood of spam, phishing, and fraudulent communication attempts.
- Internet-facing infrastructure visibility** — Publicly accessible domain and infrastructure information may assist attackers during reconnaissance activities.
- Unsigned DNSSEC observation** — The absence of DNSSEC signing was identified as a potential DNS security consideration; however, no exploitation or DNS-related attack activity was observed.
- Limited network reconnaissance** — Basic network scanning activity was documented, but insufficient scan results were available to determine exposed services, vulnerabilities, or security weaknesses.

Overall, the identified risks relate primarily to **information exposure and reconnaissance visibility**, rather than confirmed security compromise.

## Recommendations

Based on the assessment findings, the following recommendations are proposed to reduce organizational exposure and improve security posture:

- Review publicly exposed employee information** — Minimize unnecessary disclosure of staff details, email addresses, and organizational information that could be leveraged by threat actors.
- **Strengthen phishing awareness training** — Conduct regular security awareness programs to help employees identify and respond to phishing, social engineering, and impersonation attempts.
- Review email security controls** — Implement and maintain effective email protection measures such as anti-phishing controls, email filtering, SPF, DKIM, and DMARC configurations.
- Evaluate DNSSEC implementation** — Assess the feasibility of enabling DNSSEC to improve DNS integrity and reduce risks associated with DNS manipulation.
- Continuously monitor external attack surface** — Regularly identify and review publicly exposed assets, domains, services, and digital footprints.
- Periodically review internet-facing systems** — Conduct routine security assessments of externally accessible applications, services, and infrastructure to identify and remediate potential weaknesses.

Implementing these recommendations will help reduce reconnaissance exposure, improve resilience against social-engineering attacks, and strengthen the organization's overall cybersecurity posture.

## References

The following tools and public platforms were used as sources of information during this assessment. Refer to **Section 5 — Tools Used** and the **Evidence** column of each finding in **Section 7 — Findings** for corresponding screenshots and supporting documentation.

| No. | Reference / Source | Purpose |
|----|--------------------|---------|
| 1 | Google Search and Bing Search | Search-engine dorking and discovery of publicly available information. |
| 2 | LinkedIn (`linkedin.com`) | Public employee profiling and organizational information gathering. |
| 3 | Instagram | Public social media intelligence and contact information discovery. |
| 4 | Wayback Machine (`web.archive.org`) | Historical website analysis and retrieval of archived web content. |
| 5 | WHOIS / CentralOps.net | Domain registration, ownership, and network lookup information. |
| 6 | BGP.he.net (Hurricane Electric BGP Toolkit) | IP address, routing, ASN, and hosting relationship analysis. |
| 7 | OSINT Framework (`osintframework.com`) | Access to categorized open-source intelligence resources and investigation tools. |
| 8 | Maltego (Community/Desktop Edition) | Relationship mapping and infrastructure intelligence analysis. |
| 9 | Nmap (executed from Kali Linux) | Network reconnaissance and host/service discovery. |

**Table 3 — Public tools and platforms referenced during the OSINT assessment.**
