# CodeAlpha_Phishing-Awareness-Training
# 🔐 Phishing Incident Investigation

## 📌 Overview

This repository documents my personal experience and practical approach to investigating phishing incidents.

When investigating a suspected phishing email, my primary focus is to determine whether the **URL, email attachment, or sender domain** is malicious. I use multiple security-analysis tools to validate indicators and gather supporting evidence before taking further action.

> ⚠️ **Safety Reminder:** Never open a suspicious or phishing URL directly in your browser. When analyzing a suspicious URL, submit it manually to an appropriate security-analysis tool instead of clicking or visiting the link.

---

## 🔎 My Phishing Investigation Process

### 1. 🌐 Check Whether the URL Is Malicious

When a phishing email contains a URL, I first investigate the URL to determine whether it has been reported as malicious or suspicious.

**Tools I use:**

- **Zscaler Zulu** — URL reputation and security analysis
- **VirusTotal** — URL and threat-intelligence analysis

**What I look for:**
- Malicious or suspicious verdicts
- Security-engine detections
- Domain reputation
- Redirects and suspicious destinations
- Other available threat-intelligence information

---

### 2. 📎 Check Whether the Attachment Is Malicious

If the email contains an attachment, I investigate the file before opening it.

**Tools I use:**

- **MD5 File Calculator** — Calculate the file's MD5 hash
- **VirusTotal** — Check the file hash and available malware detections

**What I look for:**
- File hash
- Antivirus detections
- Malware classifications
- Suspicious file characteristics
- Whether the hash has previously been associated with malicious activity

> ⚠️ **Important:** Avoid opening unknown or suspicious attachments on your normal workstation. Use appropriate isolated analysis environments and security tools.

---

### 3. 📧 Check the Reputation of the Sending Domain

I also investigate the domain associated with the sender to determine whether it has a suspicious or poor reputation.

**Tool I use:**

- **Cisco Talos Intelligence** — Domain and reputation information

**What I look for:**
- Domain reputation
- Historical reputation information
- Suspicious domain characteristics
- Other available threat-intelligence indicators

---

## 🛠️ Tools Used

| Purpose | Tool |
|---|---|
| URL reputation | Zscaler Zulu |
| URL & file analysis | VirusTotal |
| File hash calculation | MD5 File Calculator |
| Domain reputation | Cisco Talos Intelligence |

---

## 🔄 Investigation Workflow

```text
                Phishing Email
                      │
                      ▼
              ┌───────────────┐
              │ Examine Email │
              └───────┬───────┘
                      │
          ┌───────────┼───────────┐
          ▼           ▼           ▼
        URL       Attachment    Sender
          │           │           │
          ▼           ▼           ▼
       Analyze       Hash       Domain
        URL          File      Reputation
          │           │           │
          ▼           ▼           ▼
       Zulu /      MD5 /      Cisco Talos
      VirusTotal  VirusTotal
          │           │           │
          └───────────┼───────────┘
                      ▼
                Investigation
                   Findings
                      │
                      ▼
             Document & Respond
```

---

## 🧠 Key Lessons From My Experience

- **Never assume a URL is safe just because the email looks legitimate.**
- **Always investigate suspicious URLs before accessing them.**
- **Analyze attachments before opening them.**
- **Check the reputation of the sending domain.**
- **Use multiple security tools rather than relying on a single verdict.**
- **Document findings and indicators of compromise (IOCs) during the investigation.**
- **Protect sensitive information when documenting real incidents.**

---

## ⚠️ Security & Privacy

This repository is intended for **security research, learning, and incident-investigation documentation**.

When documenting real phishing incidents, do not publish:

- Passwords or authentication tokens
- Private or confidential email content
- Personal information
- Internal company information
- Sensitive IP addresses or infrastructure details
- Confidential investigation evidence

Use sanitized or fictional examples when sharing investigation results publicly.

---

## 🎯 Objective

The goal of this project is to document a practical and repeatable approach to phishing investigation and demonstrate how security-analysis tools can be used to validate suspicious URLs, attachments, and sender domains.

---

## 📚 Tools & Resources

- Zscaler Zulu — URL reputation analysis
- VirusTotal — Threat intelligence and file/URL analysis
- MD5 File Calculator — File hash calculation
- Cisco Talos Intelligence — Domain and reputation information
