# Phishing Email Analysis Lab

A practical cybersecurity project focused on analyzing phishing, suspicious, spam, and legitimate emails using publicly available email corpora.

The objective of this project is to develop and demonstrate practical SOC analyst skills in email security investigation.

---

## Objectives

This project focuses on:

- Email header analysis
- SPF analysis
- DKIM analysis
- DMARC analysis
- Received header investigation
- Sender and Reply-To analysis
- Email infrastructure investigation
- URL analysis
- Attachment analysis
- IOC extraction
- Phishing detection
- Social engineering analysis
- MITRE ATT&CK mapping
- SOC investigation documentation

---

## Investigation Workflow

Each email is investigated using a consistent workflow:

```
Email
  │
  ▼
Header Extraction
  │
  ▼
Sender Analysis
  │
  ▼
Received Header Analysis
  │
  ▼
SPF / DKIM / DMARC
  │
  ▼
URL & Attachment Analysis
  │
  ▼
IOC Extraction
  │
  ▼
Social Engineering Analysis
  │
  ▼
MITRE ATT&CK Mapping
  │
  ▼
Final Verdict
  │
  ▼
SOC Recommendations
```

---

## Repository Structure

```
phishing-email-analysis/
│
├── README.md
│
├── methodology/
│   ├── email-header-analysis.md
│   └── investigation-workflow.md
│
└── cases/
    ├── 001-phishing-email/
    ├── 002-phishing-email/
    └── 003-phishing-email/
```

---

## Skills Demonstrated

### Email Security

- Email header analysis
- SPF
- DKIM
- DMARC
- Received headers
- Sender authentication
- Email spoofing detection

### Threat Analysis

- URL investigation
- Domain analysis
- IP analysis
- IOC extraction
- Social engineering detection
- Phishing classification

### SOC Skills

- Alert investigation
- Evidence collection
- Investigation documentation
- Incident classification
- Recommended response actions
- MITRE ATT&CK mapping

---

## Tools Used

- VirusTotal
- ANY.RUN
- UrlScan.io
- MXToolBox

---

## Data Sources

This project uses publicly available email corpora for educational and research purposes.

The original dataset and its license are referenced in each applicable case.

Original email data is not redistributed unless the applicable dataset license explicitly permits redistribution.

---

## Disclaimer

This project is intended for cybersecurity education, defensive security research, and SOC analyst training.

All analysis is performed on publicly available datasets or data for which analysis is authorized.

---

## Author

Ahmed Alsiddig - Cybersecurity / SOC Analyst Portfolio

LinkedIn: https://www.linkedin.com/in/ahmed-alsiddig-6a0801287