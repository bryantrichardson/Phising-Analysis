# Phising Analysis

## Description
In this blog post, I will be looking at an email to determine if it is a phishing attempt or not. I will accomplish this by using an Ubuntu VM I configured and looking at the email in Sublime Text. I will also be using open source sites such as VirusTotal, CyberChef, and whois.domaintools. I will document my analysis using this <a href="https://docs.google.com/document/d/1x6iyFD8RMnvcib08EjNJcqGKYUyPSI5aYdJ1Nq38E6g/edit">template.</a><br>

Below I will provide screenshots of the process I take to analyze the email. It will not be a complete step-by-step guide, but will cover the most important parts of the analysis. I will include a link to the template at the very end in case you want to see the report in its entirety.

Thanks for clicking on this/reading, hope the rest of your day/night is swell :).<br>

(For transparency, this Ubuntu setup and phishing challenge/analysis is apart of <a href="https://academy.tcm-sec.com/p/security-operations-soc-101">TCM-Security SOC 101 course</a>.)

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
<img width="600" alt="pa-challenge-2" src="https://github.com/user-attachments/assets/e879fe90-dace-4919-bb32-f57b3fc10bbb">
<br> 
Pictured in the screenshot below is the email pulled up in Sublime Text. It has all the relevant headers as well as x-headers such as "X-Sender-IP". This header is a key one to note down so I can later use whois.domaintools to figure out more about this IP. Another relevant header is the Content-Transfer-Encoding header that denotes this email uses base64 for the message. Using CyberChef, we could have decoded this email's message and found that same defanged link from above referencing the "login to your Microsoft account" link. <br>
<img width="1200" alt="pa-challenge-1" src="https://github.com/user-attachments/assets/119d8696-ef24-478e-9ba5-23c87abb5269">
<br>
The whois.domain screenshot below is the search of the sender's IP previously noted down from the Sublime Text screenshot. The IP is a Microsoft IP based out of the Netherlands, so it appears to make sense in regards to emailing about an Outlook account. Further investigation into the defanged link is needed though.<br>
<img width="600" alt="pa-challenge-domaintools" src="https://github.com/user-attachments/assets/23b5a05c-7540-41a4-af44-2410cc44966e">
<br>
The two screenshots below are regarding the defanged url from above being put into VirusTotal (first screenshot) and urlscan.io (second screenshot). VirusTotal had 3 vendors flag it for phishing. Only 18 of the vendors had reviewed it, so a pretty alarming notice. The interesting thing about urlscan.io's screenshot is the fact that this url is based out of Germany. There very well could be an explanation for this, but considering the .edu sender email is originating from a university in Egypt, the domain lookup on the sender's IP goes to a Netherlands host, and this url being out of Germany does not instill any faith in this email being an actual legit email. I would agree with the three vendors on VirusTotal and agree this email as a whole is a phishing attempt.
<br>
<img width="600" alt="pa-challenge-virustotal" src="https://github.com/user-attachments/assets/49930dde-be68-4584-a178-d92274e58cc6">
<img width="600" alt="pa-challenge-urlscan" src="https://github.com/user-attachments/assets/126375d1-05ac-4d89-808e-bf4d31cf6c0f"><br>

## Complete Report
* <a href="https://docs.google.com/document/d/1Kml8LcMpSTAxR9_Y4GtJFYlPo5lFweDeqgi1Cjr3L0A/edit">**Report** (TCM Challenge)</a>



