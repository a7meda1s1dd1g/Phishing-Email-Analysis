# CASE-006 — Phishing Email

**Verdict:** True Positive
**Confidence:** High

### Email

* **From:** `ylrwncyhzayuok.06749627686688@2ghuj7.2ghuj7.igryzu.us`
* **Subject:** Encoded/obfuscated subject
* **Sender IP:** `192.236.246.75`
* **Return-Path:** Missing
* **Reply-To:** Missing

### Authentication

* **SPF:** PASS
* **DKIM:** PERMERROR
* **DMARC:** Missing

SPF passed, while DKIM returned a permanent error and no usable DKIM signature was found. DMARC was not present.

### URL

`https://storage.googleapis.com/whilewait/brightway.html?...`

* **VirusTotal:** 8/92 security vendors flagged the URL as malicious.

### Conclusion

The email was classified as a **True Positive phishing email**, primarily because the embedded URL was flagged as malicious by **8/92 VirusTotal security vendors**. The highly unusual sender address, encoded subject, and DKIM/DMARC authentication issues provide additional suspicious context, while SPF PASS does not rule out phishing.
