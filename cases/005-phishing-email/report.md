# CASE-005 — Suspicious Email

**Verdict:** Suspicious / Inconclusive
**Confidence:** Medium

### Email

* **From:** `anawoolery@linksofttech.com`
* **Sender:** `Google Calendar <calendar-notification@google.com>`
* **Subject:** `Invitation: Dear Quote Number QGFM33063 approval granted @ Fri Jun 5, 2026 2:29am (GMT-4)`
* **Sender IP:** `209.85.161.69`
* **Return-Path:** Missing
* **Reply-To:** `anawoolery@linksofttech.com`

### Authentication

* **SPF:** None
* **DKIM:** PASS
* **DMARC:** None

DKIM authentication passed. SPF and DMARC returned no result; these should not be treated as authentication failures.

### URL

`https://calendar.google.com/calendar/event?...`

* **ANY.RUN:** Malicious activity reported; the server rejected the request because it was malformed.

### Conclusion

The email contains suspicious sender information and a URL that produced a malicious-activity alert in ANY.RUN. However, the available evidence is insufficient to definitively classify the email as phishing because the URL is hosted on `calendar.google.com`, DKIM passed, and the ANY.RUN result indicates a malformed request rather than confirmed malicious behavior.
