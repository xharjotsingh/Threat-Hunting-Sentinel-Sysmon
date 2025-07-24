## T1059 - Command-Line Execution

- Used `cmd.exe /c whoami`
- Triggered Sysmon Event ID 1 (Process Creation)
- Later detected via KQL

Screenshot:
[cmd.exe /c whoami](../docs/screenshots/t1059_cmd_execution.png)

## T1086 - Encoded PowerShell

- Used base64 to obfuscate script
- Ran it via `powershell.exe -enc ...`
- Log shows encoded script execution

Screenshot:
[Encoded PowerShell](../docs/screenshots/t1086_encoded_powershell.png)

## T1566 - LOLBin Phishing Simulation

- Used `certutil` and `mshta` to simulate download-based phishing
- Setup a simple HTTP server (on host) using [python -m http.server 8000]
- Triggered Event ID 1 (Process Creation)

Screenshot:
[certutil + mshta phishing](../docs/screenshots/t1566_phishing.png)
