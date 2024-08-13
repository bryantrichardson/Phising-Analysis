# Splunk Alerts and Dashboards with Atomic Red Team

## Description
In this project, I play around with a setup of 4 virtual machines (VMs) to simulate attacks on endpoints whether that be servers or individual machines. The setup is by MyDFIR on YouTube. He does some attacks to show that the setup works, but I will be doing other attacks. These attacks are from AtomicRedTeam sumn sumn sumn,  could be a whole lot better, but just to have sumn written here

The 4 attacks I will be doing are a brute force from the Kali machine targetting the Windows 10 machine trying to crack a password of a user using the tool Crowbar. The second will be creating a local valid account on the Windows 10 machine using AtomicRedTeam atomic number T1078.003. The third will be finding unsecured credentials on the Windows 10 machine using AtomicRedTeam atomic number T1552.001. 

## Tools Used
* **Splunk**
* **SPL**
* **AtomicRedTeam**
* **Windows Powershell**
* **Active Directory**
* Sumn else?

## Environments Used
* **Splunk Server** (VM)
* **Active Directory Domain Controller** (VM)
* **Windows 10 Machine** (Target VM)
* **Kali Attacker Machine** (Attacker VM)

## Diagram 
<img width="410" alt="Diagram adp pt1" src="https://github.com/user-attachments/assets/3edf66d0-706c-48a5-bae6-0200fa77bed3">
