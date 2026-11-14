# Azure Cloud SIEM Lab: Splunk Enterprise Deployment

## 🎯 Objective
To deploy a Windows Server 2022 Virtual Machine on Microsoft Azure and install Splunk Enterprise SIEM to monitor and analyze Windows Event Logs (including RDP brute-force attack attempts).

## 🛠️ Technologies Used
* **Cloud Platform:** Microsoft Azure (IaaS)
* **Operating System:** Windows Server 2022
* **SIEM Tool:** Splunk Enterprise
* **Protocols:** RDP (Port 3389)

## 🚀 Steps Executed
1. Provisioned a Windows Server 2022 VM (Standard_B2s_v2) in the Azure Central India region.
2. <img width="1920" height="1080" alt="clip1" src="https://github.com/user-attachments/assets/48a97028-5163-414f-b34f-cc7ad062fe27" />
3. Configured Azure Network Security Group (NSG) to allow inbound RDP traffic.
4. Successfully established a Remote Desktop Connection (RDP) via Public IP.
5. <img width="1920" height="1080" alt="clip2" src="https://github.com/user-attachments/assets/0f25bf6b-0692-4d89-8f58-b88ca3c6825b" />
## 🔍 Phase 1: Generating Raw Logs (Event Viewer)
* Configured Windows Audit Policy (`secpol.msc`) to log failed logon attempts.
* <img width="1920" height="1080" alt="activity log" src="https://github.com/user-attachments/assets/56c29953-5516-45e5-9ea7-987df5b3e56d" />
* Simulated a brute-force RDP attack using a dummy account (`intruder`).
* Verified the raw logs in Windows Event Viewer (Event ID 4625).
* <img width="1920" height="1080" alt="event viewer" src="https://github.com/user-attachments/assets/e81d9c23-68a6-451a-b05a-5f6fc8f2fd95" />
## 📊 Phase 2: SIEM Ingestion & Analysis (Splunk)
* Installed Splunk Enterprise on the Windows Server.
* <img width="1920" height="1080" alt="splunk install" src="https://github.com/user-attachments/assets/dae174c4-2a84-432d-b17f-7feaa7fef1a4" />
* Configured Data Inputs to monitor local Windows Security logs.
* <img width="1920" height="1080" alt="splunk2eventsview" src="https://github.com/user-attachments/assets/fd0005ac-bcaf-40f3-84ce-e494078b2858" />
* Queried the logs in Splunk using SPL: `source="WinEventLog:Security" EventCode=4625`
* <img width="1920" height="1080" alt="splunk3event4625" src="https://github.com/user-attachments/assets/d74bd12e-3918-4e01-ab0b-5e3d006aea34" />
* Successfully analyzed the attacker's IP, Account Name, and Failure Reason.
* <img width="1920" height="1080" alt="splunk4failedlogon" src="https://github.com/user-attachments/assets/b3936167-20e3-497b-86cf-16bf0fbafb19" />

