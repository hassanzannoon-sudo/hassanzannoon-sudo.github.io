# Incident Report: Suspicious Process Execution

**Project:** Endpoint Detection (Sysmon + ELK)
**Author:** Hassan Zannoon
**Date:** 2025-12-09

## Summary
Detected a suspicious process execution (PowerShell) on host WIN-VM-01. Sysmon EventID 1 and PowerShell module logs indicate execution of encoded commands and creation of persistence artifacts.

## Timeline
- 2025-11-25 14:05 IST — Suspicious PowerShell process created.
- 2025-11-25 14:06 IST — Registry changes recorded (EventID 13).
- 2025-11-25 14:08 IST — Alert triggered and investigated.

## Detection
- Events: Sysmon EventID 1 (Process Create), EventID 13 (Registry SetValue)
- Evidence: sysmon-events.json, kibana/screenshot-powershell.png

## Investigation Steps
1. Pull full Sysmon event logs for process tree.
2. Identify parent process and command line.
3. Check for any network connections initiated by the process (EventID 3).
4. Search for persistence (registry autoruns, scheduled tasks).
5. Isolate host if active malicious behavior confirmed.

## Findings
- Encoded PowerShell command observed.
- Registry autorun key created under HKCU\Software\Microsoft\Windows\CurrentVersion\Run.
- Network connection to suspicious domain observed but uncertain if beaconing.

## Containment & Remediation
- Isolate host WIN-VM-01 from network for deeper forensics.
- Remove persistence keys and disable suspicious scheduled tasks.
- Reset affected user credentials and scan for additional indicators.

## Recommendations
- Deploy enhanced PowerShell logging and constrained language mode.
- Add IOC blocklist and alerting for similar process creation patterns.

## Evidence Files
- sysmon-events.json
- kibana/powershell.png
- investigation-report.md
