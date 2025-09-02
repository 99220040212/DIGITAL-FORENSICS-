# 🔍 Analysis of *Ex. No. 4 – Email Header Analysis & Spoofing Detection using MHA*

## 📖 Overview
Email header analysis helps investigators detect **spoofing, phishing, or tampering** by examining metadata such as sender details, server hops, timestamps, and authentication results.  
The **Mail Header Analyzer (MHA)** tool simplifies this process by parsing and analyzing raw email headers.

---

## 🧩 Steps for Email Header Analysis

### 1. Access the Email Header
- **Gmail** → Open email → ⋮ (More) → *Show original*  
- **Outlook** → File → Properties → *Internet headers*  
- **Yahoo** → ⋮ (More) → *View raw message*  

---

### 2. Copy the Email Header
- Copy the **entire header text**.  
- Contains metadata about sender, servers, and message journey.  

---

### 3. Identify Key Fields
- **From** → Sender’s email address  
- **To** → Recipient’s email address  
- **Date** → Time email was sent  
- **Subject** → Email subject line  
- **Return-Path** → Bounce address  
- **Received** → Server hop sequence (critical for analysis)  
- **Message-ID** → Unique identifier  
- **SPF/DKIM/DMARC** → Authentication checks  

---

### 4. Analyze Received Fields
- Shows **path of email delivery**, listed in reverse order.  
- Each line includes:  
  - Sending server (IP/hostname)  
  - Receiving server  
  - Timestamp  

---

### 5. Check IPs & Hostnames
- Use **WHOIS / IP lookup** tools.  
- Verify if IP addresses and hostnames align with legitimate mail servers.  
- Look for anomalies like unknown or mismatched servers.  

---

### 6. Examine SPF, DKIM & DMARC
- **SPF** (Sender Policy Framework)  
  - ✅ Pass → Authorized sender  
  - ❌ Fail → Possible spoofing  
- **DKIM** (DomainKeys Identified Mail)  
  - ✅ Pass → Email not altered  
  - ❌ Fail → Possible tampering  
- **DMARC** (Domain-based Message Authentication, Reporting & Conformance)  
  - Uses SPF + DKIM for policy enforcement  
  - Fail → Strong indicator of spoofing  

---

### 7. Inspect Message-ID
- Usually contains sending domain.  
- Mismatch with sender’s claimed domain → suspicious.  

---

### 8. Look for Anomalies
- **Domain mismatches** between *From, Return-Path, Message-ID*.  
- **Unfamiliar IPs** in Received headers.  
- **Odd timestamps** indicating delays or rerouting.  

---

### 9. Use Automated Tools
- **MXToolbox**  
- **Google G Suite Toolbox**  
- **Other online header analyzers**  

These tools parse headers automatically and highlight inconsistencies.  

---

### 10. Document & Report
- Record findings for investigation.  
- Report suspicious emails to **IT/security teams** or the **email provider**.  

---

## 📝 Example Header Analysis
