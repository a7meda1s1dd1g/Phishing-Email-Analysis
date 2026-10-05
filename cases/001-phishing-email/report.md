# CASE-001 — Phishing Email Analysis

## 1. Case Information

| Field          | Value                 |
| -------------- | --------------------- |
| Case ID        | CASE-001              |
| Dataset        | [Corpus name]         |
| Email ID       | [Email ID / filename] |
| Analysis Date  | 2026-10-06            |
| Classification | Phishing              |
| Confidence     | High                  |

---

# 2. Executive Summary

The analyzed email was classified as **phishing** based on multiple indicators identified during header, sender, authentication, content, and infrastructure analysis.

The investigation identified the following key indicators:

* [Indicator 1]
* [Indicator 2]
* [Indicator 3]

---

# 3. Email Information

| Header      | Value |
| ----------- | ----- |
| From        |       |
| To          |       |
| Reply-To    |       |
| Return-Path |       |
| Subject     |       |
| Date        |       |
| Message-ID  |       |

---

# 4. Header Analysis

## From

```text
[From header]
```

### Analysis

[Explain whether the sender identity appears legitimate.]

---

## Reply-To

```text
[Reply-To header]
```

### Analysis

[Compare Reply-To with From.]

---

## Return-Path

```text
[Return-Path header]
```

### Analysis

[Explain the relationship between Return-Path and From.]

---

# 5. Received Header Analysis

## Received Chain

```text
[Paste relevant Received headers]
```

### Extracted Infrastructure

| Hop | IP | Hostname | Timestamp | Observation |
| --- | -- | -------- | --------- | ----------- |
| 1   |    |          |           |             |
| 2   |    |          |           |             |
| 3   |    |          |           |             |

### Analysis

[Explain the email's delivery path and identify the earliest relevant external infrastructure.]

---

# 6. Email Authentication

## SPF

**Result:** [PASS / FAIL / SOFTFAIL / NONE]

### Analysis

[Explain what the SPF result means.]

---

## DKIM

**Result:** [PASS / FAIL / NONE]

**Signing Domain:**

```text
[domain]
```

**Selector:**

```text
[selector]
```

### Analysis

[Explain the DKIM result.]

---

## DMARC

**Result:** [PASS / FAIL / NONE]

**Policy:**

```text
[policy]
```

### Analysis

[Explain the DMARC result and alignment.]

---

# 7. Authentication-Results

```text
[Relevant Authentication-Results header]
```

### Analysis

[Correlate SPF, DKIM and DMARC.]

---

# 8. Sender Infrastructure

## Sender IP

```text
[IP]
```

| Attribute      | Value |
| -------------- | ----- |
| IP             |       |
| Reverse DNS    |       |
| ASN            |       |
| Organization   |       |
| Country/Region |       |

### Analysis

[Explain whether the infrastructure is consistent with the claimed sender.]

---

# 9. URL Analysis

| URL | Domain | Suspicious | Reason |
| --- | ------ | ---------- | ------ |
|     |        |            |        |

### Analysis

[Explain the URL indicators.]

---

# 10. Attachment Analysis

| Filename | Type | Size | SHA-256 | Suspicious |
| -------- | ---- | ---: | ------- | ---------- |
|          |      |      |         |            |

### Analysis

[Explain attachment-related indicators.]

---

# 11. Social Engineering Analysis

| Indicator          | Present | Evidence |
| ------------------ | ------- | -------- |
| Urgency            |         |          |
| Threat             |         |          |
| Account suspension |         |          |
| Credential request |         |          |
| Payment request    |         |          |
| Impersonation      |         |          |

### Analysis

[Explain the psychological/social-engineering techniques used.]

---

# 12. Indicators of Compromise

## IP Addresses

```text
[IP]
```

## Domains

```text
[domain]
```

## URLs

```text
[url]
```

## Email Addresses

```text
[email]
```

## File Hashes

```text
[SHA-256]
```

---

# 13. MITRE ATT&CK

### Technique

**T1566 — Phishing**

### Sub-technique

[Example: T1566.002 — Spearphishing Link]

### Evidence

[Explain exactly why the technique applies.]

---

# 14. Detection Opportunities

Potential SOC detections:

* Detect suspicious sender-domain mismatches.
* Detect suspicious Reply-To domains.
* Detect malicious URLs.
* Detect known malicious sender IPs.
* Detect phishing-related subjects combined with external URLs.
* Detect messages failing DMARC when impersonating protected domains.

---

# 15. Recommended Response

1. Quarantine the email.
2. Search for additional recipients.
3. Search DNS/proxy logs for the identified domains.
4. Search endpoint telemetry for related activity.
5. Block confirmed malicious indicators.
6. Reset credentials if credential submission is confirmed.
7. Document the incident.

---

# 16. Final Verdict

**Classification:** PHISHING

**Confidence:** HIGH

### Key Evidence

1. [Evidence]
2. [Evidence]
3. [Evidence]

### Analyst Conclusion

[Write a concise evidence-based conclusion explaining why the email was classified as phishing.]

---

# 17. References

* [Dataset/corpus]
* [Relevant threat intelligence sources]
* [Other references]

