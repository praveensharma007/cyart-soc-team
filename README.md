# SOC Analyst Practical Project – Week 2

# 📌 Project Overview

This project demonstrates Security Operations Center (SOC) workflows including:

Alert monitor
Incident classification
Alert triage
Incident response
Evidence collection and documentation

The implementation uses real tools like Wazuh SIEM, TheHive, and threat intelligence platforms.

📖 Theoretical Knowledge
# 🔎 Investigation Details

- Checked SSH logs for failed login attempts  
- Verified source IP reputation using threat intelligence  
- Observed repeated login attempts pattern  
- Confirmed no successful login  
- Classified as brute-force attack  

Conclusion: True Positive alert

# 🔴 Alert Priority Levels

Alerts are categorized based on severity and impact:

Critical → Ransomware, active exploitation
High → Unauthorized admin access
Me → Brute-force attempts
Low → Port scans

# 📊 Prioritization Criteria
Asset criticality
Exploit availability
Business impact

# 📐 CVSS Example
Log4Shell (CVE-2021-44228) → Score: 9.8 → Critical

# ⚖️ Alert Priority Justification

The alert was marked as Medium because:
- No successful compromise observed  
- Activity limited to login attempts  
- No lateral movement detected  
- Target system was not critical  

If successful login occurred → Priority would be High/Critical

# ✅ Alert Validation

- Checked login success → No  
- Checked unusual behavior → Yes  
- Checked frequency → High attempts  
Final Decision: True Positive (Brute-force attempt)

# 🧠 Incident Classification
Malware
Phishing
DDoS
Insider Threat
Data Exfiltration

# 🧩 Frameworks Used
MITRE ATT&CK
ENISA Taxonomy
In

# 📎 Metadata
Source IP
Timestamp
File Hash (IOC)
Target System

# ⚡ Incident Response Lifecycle
Preparation
Identification
Containment
Eradication
Recovery
Lessons Learned

# 🛠️ Tools Used
Wazuh (SIEM & Detection)
TheHive (Incident Management)
VirusTotal (Threat Intelligence)
AlienVault OTX (IOC Validation)
Metasploit (Attac
CrowdSec (Threat Blocking)

# 🔄 SOC Workflow (Step-by-Step)
Alert generated in Wazuh
Alert reviewed by SOC Analyst
Priority assigned
Triage performed
Threat intelligence
Incident ticket created
Response action taken
Documentation completed
Lessons learned recorded

# 📊 Alert Management Example
Alert ID	Description	Source IP	Priority	Status
002	Brute-force SSH	192.168.1.100	Medium	Open

# 🔍 Alert Triage & Validation
Analyzed brute-force SSH alert in Wazuh
Identified repeated failed login attempts
Validated source IP using threat intelligence tools
Determined alert as True Positive

# 🧩 MITRE ATT&CK Mapping
Technical ID	Name	Description
T1110	Brute Force	Multiple login attempts
T1190	Exploit	Initial access

# 🛡️ Incident Report – Brute Force Attack
Summary

A brute-force SSH attack was detected targeting a Linux server. Multiple failed login attempts were observed from IP 192.168.1.100.

Timeline
11:00 – Multiple failed login attempts
11:05 – Alert generated
11:10 – Suspect
11:15 – Monitoring and containment

Indicators of Compromise (IOCs)
Source IP: 192.168.1.100
Activity: Repeated failed SSH logins
Response Actions
Monitored system activity
Blocked suspicious IP
In
Recommendations
Enable account lockout
Use SSH key authentication
Disable root login

# 🧾 Evidence Collection
Item	Description	Collected By	Date	Hash Value
Memory Dump	Server-X Dump	SOC Analyst	2025-08-18	SHA256...lls including monitoring, detection, triage, and incident response.

# 📌 Conclusion

This project demonstrates practical SOC analyst skills including alert monitoring, triage, incident response, and documentation using real-world tools.

The workflow reflects real SOC operations and highlights the importance of quick detection, proper prioritization, and structured response.
