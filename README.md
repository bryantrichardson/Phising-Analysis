# Splunk Alerts and Dashboards with Atomic Red Team

## Description
In this project I configure four virtual machines (VMs)- a Windows Domain Controller Server, a Splunk Server, a Windows10 Target Machine, and a Kali Attacker Machine. I setup Atomic Red Team (ART) with the ability to attack the two servers and the target machine in order for me to see the telemetry generated in my Splunk instance. After reviewing the telemetry, I then create alerts for the specific attacks and use these alerts to create dashboards. 

The initial setup of this project is created by MyDFIR on YouTube. He does some attacks on the machines to prove the setup works, but I will be doing different attacks. The attacks I have chosen have the atomics of T1078.003, T1087.001, and T1021.001. In order, these attacks create a valid local account with admin privileges, discover/enumerate all valid local accounts, then use remote desktop protocol (RDP) with valid accounts to manipulate the machine into logging the attacker in.

In my documentation for this project, I genuinely tried to use Splunk Search Processing Language (SPL) to refine the queries to only show the adversarial telemetry. In some instances it was not completely possible, but I did not simply block RDP for instance to "solve" the problem. The same goes for some of the attacks done by ATR are blocked by Windows Firewall/Defense, but I did not disable the firewall due to it not being a practical solution. 

Below is the documentation for this project. It is not necessairly a step-by-step process in how the whole project was completed, but more of an overview of how I was able to generate the telemetry and create alerts/dashboards for the attacks.

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
