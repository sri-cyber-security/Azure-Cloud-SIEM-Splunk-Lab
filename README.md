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
6. *(Pending)* Install Splunk Enterprise and configure data inputs for local Windows Event Logs.
7. *(Pending)* Create a monitoring dashboard for failed logon attempts (Event ID 4625).
