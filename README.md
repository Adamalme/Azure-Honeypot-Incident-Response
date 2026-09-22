# Azure-Honeypot-Incident-Response
Real honeypot attack forensic analysis - 69,191 events, multi-country attackers, incident response report


# Azure Honeypot - Incident Response Report

**For hiring managers:** This portfolio demonstrates real forensic analysis 
skills without requiring a degree. Complete attack investigation from initial 
breach to evidence destruction.

## Project Overview
I conducted a real honeypot security project by intentionally exposing an Azure VM 
(sql-labuser) to the public internet to study attacker behavior and techniques.

## Attack Summary
- **Duration:** August 30 - September 15, 2026
- **Attackers:** 8 coordinated threat actors from Netherlands and Philadelphia
- **Impact:** 69,191 logged events, 6 compromised accounts, complete attack chain
- **Detection:** Microsoft Sentinel custom detection rules (KQL queries)

### **4. Add "Why This Matters" Section** (one paragraph, employer perspective)

```markdown
## Why This Matters
Most security professionals never analyze a real attack. I did. This project 
proves I can: collect forensic data at scale, correlate events across multiple 
sources, identify attack patterns, apply security frameworks in practice, and 
document findings professionally. No degree required - just curiosity and 
persistence.
```

---

### **5. Add Links to Your Files** (make it clickable)

In "What This Project Contains", change to:

```markdown
### 1. Complete Incident Response Report
- [Executive Summary](Incident_Report_Final.md#executive-summary)
- [Phase 8: Forensic Analysis](Incident_Report_Final.md#phase-8)
- [Phase 9: MITRE ATT&CK Mapping](Incident_Report_Final.md#phase-9)
- [Phase 10: Final Report](Incident_Report_Final.md#phase-10)

### 2. KQL Queries
- [Query 1: MySQL Commands](KQL_Queries/Query1_MySQL_Commands.kql)
- [Query 2: Windows Logons](KQL_Queries/Query2_Windows_Logons.kql)
- [Query 3: Process Execution](KQL_Queries/Query3_Process_Execution.kql)
- [Query 4: Network Connections](KQL_Queries/Query4_Network_Connections.kql)
- [Query 5: File Access](KQL_Queries/Query5_File_Access.kql)
- [Query 6: Registry Changes](KQL_Queries/Query6_Registry_Changes.kql)
- [Query 7: Master Timeline](KQL_Queries/Query7_Master_Timeline.kql)
```

### **FINAL VERSION (with all improvements):**

## What This Project Contains

### 1. Complete Incident Response Report
- Executive Summary
- Phase 8: Forensic Analysis (7 detailed queries)
- Phase 9: MITRE ATT&CK Framework Mapping
- Phase 10: Final Incident Response Report

### 2. KQL Queries (7 queries)
All queries used to analyze the attack:
- Query 1: MySQL Malicious Commands (221 events)
- Query 2: Windows Logon Compromise (8 attacker IPs)
- Query 3: Process Execution (149+ suspicious processes)
- Query 4: Network Connections (1,642 events)
- Query 5: File Access & Modifications (12,726 events)
- Query 6: Registry Changes & Evidence Destruction (8,012 deletions)
- Query 7: Master Timeline (69,191 total events)

### 3. CSV Export Data
Raw forensic data exported from Microsoft Sentinel for each query

## Key Findings
- Attackers used brute force, then established persistence
- Multi-stage attack: enumeration → exploitation → persistence → cleanup
- 12,700+ files modified, 8,012 registry keys deleted (evidence destruction)
- All traffic stayed within Azure infrastructure (sophisticated TTPs)

## Attack Phases Identified
1. **Brute Force** (Aug 30-31): 156 failed attempts before success
2. **Active Exploitation** (Sep 1-8): SQL commands, process execution, file access
3. **Persistence** (Sep 8-11): Registry keys, backdoors installed
4. **Evidence Destruction** (Sep 11-14): Deleting logs and evidence
5. **Egress** (Sep 14-15): Final exfiltration and cleanup

## MITRE ATT&CK Techniques
- T1110: Brute Force
- T1078: Valid Accounts
- T1059: Command and Scripting Interpreter
- T1547: Boot or Logon Autostart Execution
- T1562: Impair Defenses
- T1070: Indicator Removal

## Tools Used
- Microsoft Azure (cloud infrastructure)
- Microsoft Sentinel (SIEM)
- KQL (Kusto Query Language - similar to Splunk SPL)
- Microsoft Defender Advanced Hunting

## How to Use This Repository
1. Read `Incident_Report_Final.md` for complete analysis
2. Review KQL queries in `KQL_Queries/` folder
3. Analyze CSV data in `CSV_Results/` folder
4. Use as reference for your own threat hunting

## Skills Demonstrated
- KQL query writing & debugging
- Forensic analysis & log correlation
- Incident response methodology
- MITRE ATT&CK framework application
- Professional report writing
- Critical security thinking

## Lessons Learned
This project taught me real-world cybersecurity skills that go beyond academic 
study. The Internet is dangerous - attackers found my exposed VM within hours. 
Real security requires constant monitoring, quick detection, and rapid response. 
Every organization needs SOC analysts and Security Engineers.

## Future Work
- Deploy T-Pot distributed honeypot
- Analyze attacks at global scale
- Study attacker patterns by region
- Build automated threat intelligence

---
*Project completed: September 2026*  
**Contact:** [https://www.linkedin.com/in/adam-alme/] | [Adamalme2@gmail.com]  
**Portfolio:** github.com/[https://github.com/Adamalme]]
