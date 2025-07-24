# Threat Hunting with Sysmon + Sentinel + MITRE Mapping

This project simulates attacker behavior (PowerShell, LOLBins techniques) in a controlled lab environment and detects it using Sysmon logs ingested into Microsoft Sentinel. The objective is to gain hands-on experience in detection engineering, threat hunting, and MITRE ATT&CK mapping.

---

## Techniques Simulated

| MITRE ID | Name                        | Description                              |
|----------|-----------------------------|------------------------------------------|
| T1059    | Command and Scripting Exec  | Command Executing in CMD                 |
| T1086    | PowerShell                  | Base64 or direct PowerShell abuse        |
| T1218    | Signed Binary Execution     | LOLBin abuse using certutil, mshta       |

---

```## Project Structure
Threat-Hunting-Sentinel-Sysmon/
├── kql/                   # KQL detection queries
│   └── T1059_CommandExec
│   └── T1086_EncodedPowerShell
│   └── T1218_LOLBins
├── sysmon-config/         # Sysmon XML config file
│   └── sysmonconfig.xml
│   └── Sysmon64.exe
├── docs/                  # Documentation
│   └── hunting-guide.md
│   └── screenshots/
│       ├── t1059_cmd_execution.png
│       ├── t1086_encoded_powershell.png
│       ├── t1218_LOLBins.png
├── README.md              # Project overview (this file)
```
