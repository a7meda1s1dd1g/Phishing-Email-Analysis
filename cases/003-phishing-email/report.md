# CASE-003 — Phishing Email

**Verdict:** True Positive
**Confidence:** High

### Email

* **From:** `test@cargillsbank.com`
* **Subject:** `Re: Notice`
* **Sender IP:** `209.85.214.227`
* **Return-Path:** Missing
* **Reply-To:** `fdvgovzin@gmail.com`

### Authentication

* **SPF:** PASS
* **DKIM:** PASS
* **DMARC:** PASS

The email passed SPF, DKIM, and DMARC authentication. However, the Reply-To address differs from the sender address and points to an unrelated Gmail account.

### URLs and Attachments

**None**

### Conclusion

The email was classified as a **True Positive phishing email** because the Reply-To address differs from the sender address and points to an unrelated Gmail account. SPF, DKIM, and DMARC passed successfully.
