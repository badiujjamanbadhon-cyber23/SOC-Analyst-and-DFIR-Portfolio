# SOC Automation & Threat Detection Lab (Wazuh SIEM)

## Project Overview
This project demonstrates the setup of an enterprise-grade open-source SIEM/XDR platform (Wazuh) to monitor network traffic, windows events, and detect security threats in real-time.

## Tools & Technologies Used
* **SIEM/XDR:** Wazuh (Manager & Dashboard)
* **Hypervisor:** VirtualBox / VMware
* **Telemetry:** Windows Event Logs, Sysmon, Linux Syslog
* **Attack Platform:** Kali Linux

## Lab Architecture
```mermaid
graph TD
    A[Kali Linux <br><b>Attacker Node</b>] -- Simulated Attack <br> (Brute Force/Malware) --> B[Windows 10/11 VM <br><b>Victim Endpoint</b>]
    B -- Transmits Telemetry <br> (Sysmon & Event Logs) --> C[Wazuh Manager <br><b>SIEM/XDR Server</b>]
    C -- Generates Alerts --> D[Wazuh Dashboard <br><b>SOC Monitoring Web UI</b>]

    style A fill:#bf2626,stroke:#333,stroke-width:2px,color:#fff
    style B fill:#1f77b4,stroke:#333,stroke-width:2px,color:#fff
    style C fill:#2ca02c,stroke:#333,stroke-width:2px,color:#fff
    style D fill:#7f7f7f,stroke:#333,stroke-width:2px,color:#fff
```
## Step-by-Step Implementation
1. Installed Wazuh Manager on a Linux environment.
2. Configured Wazuh Agents on Windows and Linux endpoints.
3. Enabled Sysmon on the Windows machine for advanced process auditing.
4. Simulated real-world attacks (like Brute Force and Malicious Execution).
5. Analyzed alerts on the Wazuh Security Dashboard.

## Key Findings & Alert Analysis
<img width="1600" height="904" alt="85a034aa-cba9-43ed-9b7f-6b9dbb593d08" src="https://github.com/user-attachments/assets/ffa14490-42b8-4fdb-bc8b-5364bb0b8996" />
