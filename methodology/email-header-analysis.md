# Email Header Analysis Methodology

## 1. Basic Header Identification

The first step is to identify the main email headers.

Important headers include:

* From
* To
* Reply-To
* Return-Path
* Subject
* Date
* Message-ID

The objective is to determine whether the sender identity appears consistent.

---

## 2. From Header

Analyze:

* Display name
* Email address
* Domain
* Possible impersonation

Questions:

* Does the display name match the email address?
* Does the domain belong to the claimed organization?
* Is the domain misspelled?
* Is the sender attempting to impersonate another organization?

---

## 3. Reply-To Header

Compare the Reply-To address with the From address.

A different Reply-To address is not automatically malicious, but it can be suspicious when it redirects replies to an unrelated domain.

---

## 4. Return-Path

The Return-Path identifies the address used for email delivery and bounce handling.

Compare:

```text
From
Reply-To
Return-Path
```

Look for unexpected domain relationships.

---

## 5. Received Headers

Received headers describe the path an email took through mail servers.

Analyze the chain from the oldest relevant external hop toward the recipient.

Record:

* IP address
* Hostname
* Timestamp
* Mail server
* Organization

Look for:

* Unexpected infrastructure
* Suspicious IP addresses
* Inconsistent hostnames
* Unusual routing
* Timestamp anomalies

---

## 6. SPF

SPF determines whether an IP address is authorized to send email for a domain.

Possible results include:

* PASS
* FAIL
* SOFTFAIL
* NEUTRAL
* NONE

Important:

> SPF PASS does not automatically mean that an email is legitimate.

The analyst should also consider domain alignment and the other authentication mechanisms.

---

## 7. DKIM

DKIM provides cryptographic authentication for email messages.

Record:

* Result
* Signing domain
* Selector

Possible results include:

* PASS
* FAIL
* NONE

---

## 8. DMARC

DMARC evaluates domain alignment using SPF and/or DKIM.

Record:

* Result
* Policy
* Header From domain
* Authenticated domains

Possible results:

* PASS
* FAIL
* NONE

---

## 9. Authentication-Results

Review the Authentication-Results header and correlate:

```text
SPF
DKIM
DMARC
```

Do not evaluate one authentication result in isolation.

---

## 10. Sender Infrastructure

Investigate the sender IP and associated infrastructure.

Record:

* IP address
* Reverse DNS
* ASN
* Organization
* Country/region

Infrastructure information should be treated as supporting evidence rather than proof of malicious activity.

---

## 11. URLs

Extract every URL from the email.

Analyze:

* Actual destination
* Displayed link
* Domain
* Redirects
* Domain impersonation
* URL shortening
* Suspicious paths

A URL should be analyzed without visiting potentially malicious content directly when safe alternatives are available.

---

## 12. Attachments

Record:

* Filename
* Extension
* MIME type
* Size
* SHA-256
* SHA-1
* MD5

Look for:

* Double extensions
* Macros
* Scripts
* Executables
* Archive files
* Password-protected files

---

## 13. IOC Extraction

Extract:

* IP addresses
* Domains
* URLs
* Email addresses
* File hashes

Store indicators separately so they can be searched or correlated later.

---

## 14. Social Engineering

Look for:

* Urgency
* Fear
* Account suspension
* Password reset requests
* Payment requests
* Fake invoices
* Delivery notifications
* Security alerts
* Credential requests
* Impersonation

---

## 15. Final Classification

Possible classifications:

* Benign
* Spam
* Suspicious
* Phishing
* Malicious

The final classification should be based on multiple pieces of evidence rather than a single indicator.

---

## 16. Evidence-Based Conclusion

Every case should answer:

1. What happened?
2. What evidence was found?
3. Why is the email suspicious or legitimate?
4. What are the relevant IOCs?
5. What should the SOC do next?
