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
<img width="1048" height="699" alt="Powershellexe" src="https://github.com/user-attachments/assets/f5a32404-dc9b-470f-b57f-1d3a7239b283" />


### Step 2
Review process details.
