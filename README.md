# Vulnerable-Management-Program-Implementalion

In this project, we simulate the implementation of a comprehensive vulnerability management program, from inception to completion.

_**Inception State:**_ the organization has no existing policy or vulnerability management practices in place.

_**Completion State:**_ a formal policy is enacted, stakeholder buy-in is secured, and a full cycle of organization-wide vulnerability remediation is successfully completed.

<img width="1536" height="1024" alt="ChatGPT Image Mar 4, 2026 at 07_13_55 PM" src="https://github.com/user-attachments/assets/2b104ca7-8880-466e-8570-c9968d8504ea" />



# Technology Utilized
- Tenable (enterprise vulnerability management platform)
- Azure Virtual Machines (Nessus scan engine + scan targets)
- PowerShell & BASH (remediation scripts)

---


# Table of Contents

- [Vulnerability Management Policy Draft Creation](#vulnerability-management-policy-draft-creation)
- [Mock Meeting: Policy Buy-In (Stakeholders)](#step-2-mock-meeting-policy-buy-in-stakeholders)
- [Policy Finalization and Senior Leadership Sign-Off](#step-3-policy-finalization-and-senior-leadership-sign-off)
- [Mock Meeting: Initial Scan Permission (Server Team)](#step-4-mock-meeting-initial-scan-permission-server-team)
- [Initial Scan of Server Team Assets](#step-5-initial-scan-of-server-team-assets)
- [Vulnerability Assessment and Prioritization](#step-6-vulnerability-assessment-and-prioritization)
- [Distributing Remediations to Remediation Teams](#step-7-distributing-remediations-to-remediation-teams)
- [Mock Meeting: Post-Initial Discovery Scan (Server Team)](#step-8-mock-meeting-post-initial-discovery-scan-server-team)
- [Mock CAB Meeting: Implementing Remediations](#step-9-mock-cab-meeting-implementing-remediations)
- [Remediation Round 1: Outdated Wireshark Removal](#remediation-round-1-outdated-wireshark-removal)
- [Remediation Round 2: Insecure Protocols & Ciphers](#remediation-round-2-insecure-protocols--ciphers)
- [Remediation Round 3: Guest Account Group Membership](#remediation-round-3-guest-account-group-membership)
- [Remediation Round 4: Windows OS Updates](#remediation-round-4-windows-os-updates)
- [First Cycle Remediation Effort Summary](#first-cycle-remediation-effort-summary)

---
### Vulnerability Management Policy Draft Creation

This phase focuses on drafting a Vulnerability Management Policy as a starting point for stakeholder engagement. The initial draft outlines scope, responsibilities, and remediation timelines, and may be adjusted based on feedback from relevant departments to ensure practical implementation before final approval by upper management.  
[Draft]
[Vulnerability Management Policy_ Draft.docx](https://github.com/user-attachments/files/25754480/Vulnerability.Management.Policy_.Draft.docx)


---
### Step 2: Mock Stakeholder Meeting – Policy Buy-In

In this phase, a **mock stakeholder meeting** was conducted with the server and infrastructure team to present the draft **Vulnerability Management Policy**. The purpose of the meeting was to review the proposed remediation timelines, gather feedback, and evaluate whether the operational teams could realistically meet the policy requirements.

During the discussion, the team raised concerns about the feasibility of remediating **critical vulnerabilities within the initial 48-hour window**, particularly in environments that require testing, change approvals, and scheduled maintenance before applying patches.

Based on this feedback, the remediation timeline for **critical vulnerabilities was adjusted from 48 hours to one week**. This modification ensures the policy remains **practical, achievable, and aligned with operational workflows**, while still maintaining a strong security posture.

This step highlights the importance of **cross-team collaboration when developing security policies**, ensuring that security requirements are both effective and operationally realistic.

### Step 3) Policy Finalization and Senior Leadership Sign-Off

After gathering feedback from the server team, the policy is revised, addressing aggressive remediation timelines. With final approval from upper management, the policy now guides the program, ensuring compliance and reference for pushback resolution.  

### Step 4: Mock Stakeholder Meeting – Initial Scan Permission (Server Team)

In this phase, a **mock meeting was conducted with the server team** to request approval for initiating **scheduled credentialed vulnerability scans**. The objective of the meeting was to explain the scanning process, address operational concerns, and ensure the scans would not negatively impact server performance or availability.

During the discussion, the server team expressed concerns about potential **resource usage and performance impact** during scanning activities. To address these concerns, both teams agreed to begin with a **pilot scan on a single server**. This approach allowed the team to monitor system performance, evaluate the scan’s impact, and validate the scanning configuration before expanding to additional systems.

To maintain security and reduce risk, the scans were configured to use **Just-in-Time (JIT) Active Directory credentials**, ensuring that privileged access is granted only when needed and for a limited period of time.

This step demonstrates the importance of **collaboration between security and infrastructure teams** when implementing vulnerability management processes, ensuring that security operations are effective while maintaining system stability.

### Step 5) Initial Scan of Server Team Assets

In this phase, an insecure Windows Server is provisioned to simulate the server team's environment. After creating vulnerabilities, an authenticated scan is performed, and the results are exported for future remediation steps.  
<img width="953" height="1245" alt="Screenshot 2026-03-04 at 7 35 37 PM" src="https://github.com/user-attachments/assets/6f62b281-31ea-4f07-8839-d88ad7e78a81" />
[First Scan][scan 1.pdf](https://github.com/user-attachments/files/25754629/scan.1.pdf)

### Step 6: Vulnerability Assessment and Prioritization

In this phase, the identified vulnerabilities were **reviewed and analyzed to determine remediation priorities**. The prioritization strategy considered factors such as **risk severity, potential impact on the organization, and ease of remediation**. This approach ensures that the most critical and easily addressable issues are resolved first while maintaining operational efficiency.

Based on the assessment, the following remediation priorities were established:

1. **Third-Party Software Removal (Wireshark)**  
   Remove unauthorized or unnecessary installations of Wireshark from systems where it is not required. Limiting such tools reduces the risk of misuse and unnecessary exposure.

2. **Windows OS Secure Configuration – Protocols & Ciphers**  
   Harden the operating system by disabling weak or outdated protocols and cryptographic ciphers to improve overall system security.

3. **Windows OS Secure Configuration – Guest Account Group Membership**  
   Review and restrict guest account privileges to ensure they are not part of sensitive or administrative groups.

4. **Windows OS Updates**  
   Apply the latest security patches and updates to address known vulnerabilities within the Windows operating system.

This prioritization framework helps ensure that **high-risk vulnerabilities are addressed efficiently while maintaining system stability and operational continuity**.

### Step 7: Distributing Remediation Tasks to Server Teams

In this phase, the **server team was provided with the vulnerability scan reports and remediation scripts** required to address the identified security issues. The remediation package included scripts designed to resolve specific vulnerabilities discovered during the initial assessment.

To support efficient remediation, clear instructions and documentation were shared with the team. The scripts were designed to be **tested in a controlled environment before deployment**, ensuring compatibility with the organization’s systems and minimizing operational risk.

<img width="1091" height="513" alt="Screenshot 2026-03-04 at 7 44 19 PM" src="https://github.com/user-attachments/assets/531aff72-0d53-4234-873c-6ae90d401f78" />














