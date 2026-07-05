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
<img width="774" height="702" alt="Github 2 Image" src="https://github.com/user-attachments/assets/aade2292-33b9-4b01-9fc4-7392b765fa3c" />
