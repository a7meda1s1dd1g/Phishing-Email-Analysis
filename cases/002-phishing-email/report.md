# CASE-002 — Phishing Email

**Verdict:** True Positive
**Confidence:** High

### Email

* **From:** `support@fatemag.com`
* **Subject:** `Occasional light-headedness addressed in this health presentation`
* **Sender IP:** `136.66.186.133`
* **Return-Path:** Missing
* **Reply-To:** Missing

### Authentication

* **SPF:** SoftFail
* **DKIM:** None — the email was not DKIM-signed.
* **DMARC:** Fail

The authentication results are suspicious and support the phishing classification.

### URL

`https://storage.googleapis.com/sbhthredd/cd`

* **VirusTotal:** PhishingDatabase flagged the URL as phishing
* **ANY.RUN:** Indicates malicious activity

### Conclusion

The email was classified as a **True Positive phishing email** due to failed email authentication and the suspicious URL, which was flagged as phishing by VirusTotal and showed malicious activity in ANY.RUN.

