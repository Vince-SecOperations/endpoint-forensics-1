# Amadey Trojan Memory Forensics Analysis

## Overview
Memory forensics investigation of a Windows 7 system infected with Amadey Trojan Stealer using Volatility3. This analysis identifies malicious processes, command and control communications, and persistence mechanisms.

## Investigation Summary

### 🔍 Key Findings
- **Malicious Process**: `lssass.exe` (PID 2748) impersonating legitimate LSASS
- **C2 Server**: `41.75.84.12:80` with active HTTP connections
- **Malware Location**: `C:\Users\0XSH3R~1\AppData\Local\Temp\925e7e99c5\lssass.exe`
- **Downloaded Payloads**: `cred64.dll` and `clip64.dll` in AppData Roaming
- **Execution Method**: Child process `rundll32.exe` used for DLL loading

### 🛠️ Tools Used
- **Volatility3** for memory analysis
- Standard Linux utilities (`strings`, `grep`) for data parsing

### 📁 Analysis Steps
1. Process enumeration with `windows.pslist`
2. Command line analysis with `windows.cmdline`
3. Network connection mapping with `windows.netscan`
4. Memory dumping and string analysis
5. File system artifact scanning with `windows.filescan`
6. Persistence mechanism investigation

### 🎯 Outcome
Successfully identified the full infection chain including initial compromise, C2 communications, payload delivery, and persistence mechanisms.

## Files Included
- `write-up-process.txt` - Detailed analysis procedure
- Screenshots/ - Volatility command outputs and findings

## Skills Demonstrated
- Memory forensics with Volatility3
- Malware analysis techniques
- Incident response procedures
- Threat hunting methodologies
