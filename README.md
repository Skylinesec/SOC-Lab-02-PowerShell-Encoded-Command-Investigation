# Overview

A simulated SOC Level 1 investigation into a PowerShell process executed with the -EncodedCommand parameter. The objective was to determine whether the execution represented malicious activity or a benign administrative action.

## Objectives
- Investigate a PowerShell alert
- Decode a Base64 command
- Analyze process creation events
- Determine whether escalation is required
- Document findings using SOC methodology

## Environment
| Component        | Technology                 |
| ---------------- | -------------------------- |
| SIEM             | Splunk Enterprise          |
| Endpoint Logs    | Sysmon                     |
| Operating System | Windows 11                 |
| Log Forwarding   | Splunk Universal Forwarder |

## Detection
PowerShell executed using the **"-EncodedCommand"** parameter.

## Investigation
### Step 1
Search for PowerShell executions.
<img width="592" height="184" alt="SPL" src="https://github.com/user-attachments/assets/7d44b7df-9154-4a7e-9561-2162c68bd52c" />

### Step 2
Review process details.
<img width="1048" height="699" alt="Powershellexe" src="https://github.com/user-attachments/assets/35ca97d7-4417-4ebc-91c8-d99759f1b3c3" />

### Step 3
Decode Base64.
<img width="880" height="222" alt="Base64" src="https://github.com/user-attachments/assets/5b8920a6-487b-4386-ace0-168b0fdffbcb" />

### Step 4
Checked for suspicious activity:
- Child processes
- Network activity
- File downloads
- Registry modifications
- Persistence

**No suspicious behavior observed.**


