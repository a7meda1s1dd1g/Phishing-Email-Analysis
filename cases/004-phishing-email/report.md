# CASE-004 — Phishing Email

**Verdict:** True Positive
**Confidence:** High

### Email

* **From:** `29764@wisut.ac.th`
* **Subject:** `Congratulations to you`
* **Sender IP:** `209.85.210.67`
* **Return-Path:** Missing
* **Reply-To:** `fdy3215@gmail.com`

### Authentication

* **SPF:** PASS
* **DKIM:** PASS
* **DMARC:** BestGuessPass

The email passed SPF and DKIM authentication. However, the Reply-To address differs from the sender address and points to an unrelated Gmail account.

### URLs and Attachments

**None**

### Conclusion

The email was classified as a **True Positive phishing email** because it requested personal information and used a Reply-To address that differs from the sender address and points to an unrelated Gmail account. SPF and DKIM passed successfully.
