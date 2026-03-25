# SOC---Simulator
## 📌 Case Details
- **Case ID:** 8816  
- **Alert Name:** Access To Blacklisted External Url Blocked By Firewall  
- **Severity:** High
- **Category:** Firewall  
- **Date:** 24 March 2026  
The alert was triggered by a phishing email containing a malicious external link and a spoofed Microsoft domaiN

##TOTAL N0 OF ALERTS
<img width="1102" height="401" alt="image" src="https://github.com/user-attachments/assets/3cf90dc3-602d-4ed0-89ba-2523338f9836" />

## ASSIGNED ALERTS
8816      Access to Blacklisted External URL Blocked by Firewall High
I chooosed this as the number one priority due to its** high impact in severity**

##Description
A firewall detected and blocked an outbound request to a URL classified as malicious or blacklisted. This may indicate user interaction with a phishing link or possible malware attempting communication with an external command-and-control server.

SourceIP = 10.20.2.17
<img width="647" height="311" alt="image" src="https://github.com/user-attachments/assets/a9a9031d-d00a-45cf-a2b0-fbc3ca24565a" />

URL response via tryhackme: <img width="862" height="481" alt="image" src="https://github.com/user-attachments/assets/617d521c-d457-4d5e-9a00-48b4a4f271f4" />
This showed the is malicious

Action = Blocked

timestamp: 03/24/2026 12:35:27.900


<img width="565" height="391" alt="image" src="https://github.com/user-attachments/assets/2803f2d7-1a16-45a3-ab74-10013092aaad" />

<img width="566" height="425" alt="image" src="https://github.com/user-attachments/assets/d399236a-74e0-44fa-95e7-37178656560a" />

<img width="543" height="238" alt="image" src="https://github.com/user-attachments/assets/b9734eec-3158-4cdf-8fdb-f48ba92c939b" />


## INCIDENT N02:
# 🛡️ Security Incident Report

<img width="1042" height="672" alt="image" src="https://github.com/user-attachments/assets/093d9905-15a0-477d-ab97-abd3eb96c353" />



## 📌 Case Details
- **Case ID:** 8815  
- **Alert Name:** Inbound Email Containing Suspicious External Link  
- **Severity:** Medium  
- **Category:** Phishing  
- **Date:** 24 March 2026  

---

## ⏰ Time of Activity 
**24 March 2026, 12:34:13 PM**

---

## 👥 Affected Entities
- **Recipient:** h.harris@thetrydaily.thm  
- **Sender:** urgents@amazon.biz  
- **Data Source:** Email Security Gateway  
- **Environment:** Corporate Email Infrastructure  

---

## 📄 Incident Summary
An inbound email containing a suspicious external link was detected by the email security system. The message impersonates Amazon and attempts to lure the recipient into clicking a malicious link under the pretense of resolving a delivery issue.  

The email uses urgency and social engineering techniques commonly associated with phishing campaigns.

---

## ✅ True Positive Justification
The alert is classified as a **True Positive** based on the following indicators:

- The sender domain (`amazon.biz`) is not a legitimate Amazon domain  
- Use of a **shortened URL (bit.ly)** to obscure the destination  
- Presence of **urgent language** to pressure the user  
- Email content matches known **phishing delivery scam patterns**  

---

## 🚨 Escalation Justification
This alert was escalated due to:

- Targeted **phishing attempt on a corporate user**  
- Risk of **credential harvesting or malware infection**  
- Potential **lateral spread within the organization**  
- Need to verify **user interaction via firewall/proxy logs**  

---

## 🔍 Investigation Actions
- Analyzed email headers and message content  
- Identified suspicious sender domain and embedded link  
- Reviewed email security logs for delivery confirmation  
- Evaluated phishing indicators and threat patterns  
- Recommended checking firewall/proxy logs for link access  

---

## 🧠 Indicators of Compromise (IOCs)
- **Sender Email:** urgents@amazon.biz  
- **Recipient Email:** h.harris@thetrydaily.thm  
- **Subject:** *Your Amazon Package Couldn’t Be Delivered – Action Required*  
- **Malicious URL:** http://bit.ly/3sHkX3da12340  
- **Attack Type:** Phishing / Social Engineering  
- **Technique:** URL Obfuscation (Link Shortener)  
- **Direction:** Inbound  
- **Timestamp:** 24 March 2026, 12:34:13 PM  

---

## 🛠️ Remediation Actions
- Block sender domain (`amazon.biz`) at the email gateway  
- Block malicious URL at firewall/proxy level  
- Conduct **mailbox sweep** for similar phishing emails  
- Review logs for any access attempts to the URL  
- Educate user on phishing awareness  
- Reset credentials if link interaction occurred  
- Strengthen email filtering and anti-phishing controls  

---

## 📊 Risk Impact Assessment
If successful, the attack could have resulted in:

- Credential compromise  
- Unauthorized system access  
- Malware infection  
- Data exfiltration  
- Internal phishing propagation  

---

## 📌 Conclusion
The email was confirmed to be a **phishing attempt impersonating Amazon**.  

Although no immediate compromise was detected, the use of a malicious link and social engineering tactics posed a significant security risk.  

**Continuous monitoring, user awareness, and improved email security controls are recommended to prevent future incidents.**

---

## 🏁 Analyst Verdict
**True Positive – Phishing Attempt (Resolved)**


## INCIDENT N03:
## 📌 Case Details
- **Case ID:** 8814  
- **Alert Name:** Access To Blacklisted External Url Blocked By Firewall  
- **Severity:** Medium
- **Category:** Phishing  
- **Date:** 24 March 2026

  ## Description
 Splunk check: <img width="1079" height="345" alt="image" src="https://github.com/user-attachments/assets/448ddf02-9d38-4f54-82f9-7de064ba8771" />

This alert was triggered by an inbound email containing an external link with potentially suspicious characteristics. The email appears to be an onboarding message sent from onboarding@hrconnex.thm to the recipient, requesting completion of a profile setup via an embedded link. 

I ran a check analyzing the sender mail, it's domain is aligned with the organization
## Analysis
Sender: onboarding@hrconnex.thm
Recipient: j.garcia@thetrydaily.thm
Subject: Action Required: Finalize Your Onboarding Profile
Link: https://hrconnex.thm/onboarding/15400654060/j.garcia
Attachment:<img width="860" height="514" alt="image" src="https://github.com/user-attachments/assets/545aef9b-028b-411b-bee3-e15d76ae3f70" />

## Observations:
1. Domain appears internal and consistent
2. No obvious typosquatting or spoofing detected
3. Email follows a legitimate onboarding theme
4. Contains embedded link requesting user action

## Attack Indicators
1. Embedded link requesting user action
2. Social engineering (onboarding scenario)
3. Potential internal domain impersonation

<img width="546" height="494" alt="image" src="https://github.com/user-attachments/assets/684c4bc4-a404-4291-93be-593c25082b37" />
<img width="545" height="143" alt="image" src="https://github.com/user-attachments/assets/8ea67406-b0eb-4209-91ab-1e7b1802323c" />

## Conclusion

Status: Suspicious – Needs Validation

This alert does not show strong indicators of phishing but requires verification of the sender and domain legitimacy. No confirmed malicious activity at this stage.



## INCIDENT N04:
## 📌 Case Details
- **Case ID:** 8817 
- **Alert Name:** Inbound Email Containing Suspicious External Link  
- **Severity:** Medium
- **Category:** Phishing  
- **Date:** 24 March 2026

## Description
This alert was triggered by an inbound email containing a suspicious external link. The email claims to be from Microsoft and notifies the recipient of an unusual sign-in attempt, urging immediate action to secure the account.
Upon analysis, the sender domain (m1crosoftsupport.co) was identified as a typosquatted domain, mimicking a legitimate Microsoft domain by replacing the letter “i” with “1”. The embedded link directs the user to a fraudulent login page intended to harvest credentials.

## Analysis
Sender: no-reply@m1crosoftsupport.co
Recipient: c.allen@thetrydaily.thm
Subject: Unusual Sign-In Activity on Your Microsoft Account
Malicious URL: https://m1crosoftsupport.co/login
IP Address (claimed): 102.89.222.143
Attachment: <img width="1062" height="351" alt="image" src="https://github.com/user-attachments/assets/615b4a21-cac0-416f-a57d-86f620ddde26" />

Indicators Identified:
Typosquatted domain (m1crosoftsupport.co)
Impersonation of Microsoft
External malicious link
Use of urgency (“secure your account immediately”)
Suspicious login alert message
<img width="845" height="470" alt="image" src="https://github.com/user-attachments/assets/894450df-e147-4a76-84e7-4a6ec6de752a" />
## CASE REPORT ATTACHMENT
<img width="435" height="456" alt="image" src="https://github.com/user-attachments/assets/e41599b9-0021-4f63-867d-91f57d22a973" />



## INCIDENT N05:
## 📌 Case Details
- **Case ID:** 8818 
- **Alert Name:** Inbound Email Containing Suspicious External Link  
- **Severity:** Medium
- **Category:** Phishing  
- **Date:** 24 March 2026

## DESCRIPTION
This alert was generated after detecting an inbound email containing a suspicious external link. As a cybersecurity student analyzing this case, the goal is to determine whether the email is part of a phishing attack or a legitimate communication.

Emails like this often require careful inspection because attackers commonly use links to trick users into visiting fake websites or entering sensitive information. During the investigation, attention should be given to the sender’s email address, the domain of the embedded link, and the overall tone of the message.
