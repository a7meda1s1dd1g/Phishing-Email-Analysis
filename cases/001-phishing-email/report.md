# CASE-001 — Phishing Email

**Verdict:** True Positive
**Confidence:** High

### Email

* **From:** `accounts@iinet.net.au`
* **Subject:** `IRAS | Internal Revenue Service/Refund #659010349`
* **Sender IP:** `203.59.1.107`
* **Return-Path:** Missing
* **Reply-To:** Missing

### Authentication

* **SPF:** PASS
* **DKIM:** None — the email was not DKIM-signed.
* **DMARC:** BestGuessPass

The missing DKIM signature and missing Return-Path/Reply-To are supporting observations, but they do not independently prove that the email is malicious.

### URL

`https://fanlink.to/tFR28R`

* **VirusTotal:** 4/91 flagged malicious
* **ANY.RUN:** 6 network threats

### IOCs

```text
IP: 203.59.1.107
Domain: fanlink.to
URL: https://fanlink.to/tFR28R
```

### Conclusion

The email was classified as a **True Positive phishing email**, primarily due to the suspicious URL and supporting malicious detections from VirusTotal and ANY.RUN. The authentication results were treated as supporting evidence rather than the primary reason for the verdict.
