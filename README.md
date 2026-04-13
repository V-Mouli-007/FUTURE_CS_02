# Phishing Email Detection & Awareness System
### 🛡️ Future Interns - Cyber Security Task 2 (2026)

## 📌 Project Overview
Phishing remains the most prevalent entry point for ransomware and data breaches. This project demonstrates a professional approach to **Email Analysis** and **Security Awareness**. As a Security Analyst, I have identified, analyzed, and classified real-world phishing samples to create an actionable awareness report for corporate environments.

---

## 🛠️ Tools & Technologies Used
* **Analysis Tools:** Google Admin Toolbox (Messageheader), MXToolbox, URLScan.io, and VirusTotal.
* **Documentation:** Markdown, Microsoft Word/PDF.
* **Methodology:** OSINT-based domain verification and social engineering identification.

---

## 🔍 Detailed Analysis Methodology
I followed a 4-step investigative process to determine the legitimacy of received emails:

### 1. Header Analysis
* **Sender Verification:** Checking the `From:`, `Return-Path:`, and `Reply-To:` fields for inconsistencies.
* **Security Protocols:** Reviewing **SPF (Sender Policy Framework)**, **DKIM (DomainKeys Identified Mail)**, and **DMARC** status to see if the email passed authentication.

### 2. Social Engineering Identification
* **Urgency/Fear:** Identifying keywords like "Immediately," "Suspended," or "Locked."
* **Authority:** Impersonating "The Security Team" or "CEO" to gain trust.
* **Generic Greeting:** Lack of personalization (e.g., "Dear Customer" instead of your actual name).

### 3. URL & Domain Investigation
* **Typosquatting:** Identifying domains like `micros0ft.com` or `secure-verify[.]com`.
* **Hidden Links:** Hovering over buttons to reveal the true destination URL behind the hyperlink.

### 4. Risk Classification
Each analyzed email is assigned a risk level based on the following matrix:

| Level | Description | Recommended Action |
| :--- | :--- | :--- |
| **Low (Safe)** | Verified sender, expected content, passes SPF/DKIM. | Proceed normally. |
| **Medium (Suspicious)** | Unknown sender or unexpected attachment; no obvious malicious links. | Report to IT; Do not open attachments. |
| **High (Phishing)** | Confirmed malicious links, spoofed headers, and urgent threats. | **Delete & Block**; Trigger Incident Response. |

---

## 📂 Repository Structure
```bash
├── samples/                # Raw phishing email text/screenshots
├── analysis/               # Header logs and URL investigation notes
├── reports/                # Final Awareness Report (PDF)
└── README.md               # Project documentation
