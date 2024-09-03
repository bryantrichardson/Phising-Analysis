# Phising Analysis

## Description
In this blog post, I will be looking at three emails to determine if they are a phishing attempt or not. I will accomplish this by using an Ubuntu VM I configured and looking at the emails in Sublime Text. I will also be using open source sites such as VirusTotal, CyberChef, and whois.domaintools. I will document my analysis using this <a href="https://docs.google.com/document/d/1x6iyFD8RMnvcib08EjNJcqGKYUyPSI5aYdJ1Nq38E6g/edit">template.</a><br>

Below I will provide screenshots of the process I take to analyze each email. It will not be a complete step-by-step guide, but will cover the most important parts of the analysis. I will include links to each of the three templates at the very end in case you want to see the reports in their entirety.

Thanks for clicking on this/reading, hope the rest of your day/night is swell :).<br>

(For transparency, this Ubuntu setup and phishing challenge/analysis is apart of <a href="https://academy.tcm-sec.com/p/security-operations-soc-101">TCM-Security SOC 101 course</a>. Only the first phishing analysis report is based on a challenge from the SOC101 course- the others are emails I have chosen from <a href="https://phishtank.org/">PhishTank.</a>)

## Tools Used
* **Sublime Text**
* **VirusTotal**
* **CyberChef**
* **Whois.domaintools**
* **PhishTank**

## Environments Used
* **Ubuntu VM**

## Screenshots
Below is a screenshot of the email in Thunderbird. It is important to note the claims of urgency with the red/bold text of "in case of ignorance, your services will be completely suspended in 24 hours according to the terms defined in our contracts." Another key detail to note is the defanged link of "hxxps[://]0[.]232[.]205[.]92[.]host[.]secureserver[.]net/lclbluewin08812/" whenever you hover your mouse over the blue text of "login to your Microsoft account." <br>
Some text will go here?
<img width="600" alt="pa-challenge-2" src="https://github.com/user-attachments/assets/e879fe90-dace-4919-bb32-f57b3fc10bbb">
<img width="1200" alt="pa-challenge-1" src="https://github.com/user-attachments/assets/119d8696-ef24-478e-9ba5-23c87abb5269">
<img width="600" alt="pa-challenge-domaintools" src="https://github.com/user-attachments/assets/23b5a05c-7540-41a4-af44-2410cc44966e">
<img width="600" alt="pa-challenge-virustotal" src="https://github.com/user-attachments/assets/49930dde-be68-4584-a178-d92274e58cc6">
<img width="600" alt="pa-challenge-urlscan" src="https://github.com/user-attachments/assets/126375d1-05ac-4d89-808e-bf4d31cf6c0f">


