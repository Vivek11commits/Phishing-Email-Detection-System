# Detection Logic

## Objective

Detect phishing emails using multiple email security indicators.

---

## Detection Conditions

- SPF = Fail
- DKIM = Fail
- DMARC = Fail
- HTTP URL detected
- Suspicious attachment
- Known phishing keywords in subject
- Suspicious sender domain

---

## Detection Workflow

Incoming Email

↓

SPF Validation

↓

DKIM Validation

↓

DMARC Validation

↓

URL Inspection

↓

Attachment Inspection

↓

IOC Extraction

↓

Risk Score Calculation

↓

Generate Alert

↓

SOC Investigation

---

## Splunk Queries

- suspicious_sender.spl
- malicious_url.spl
- attachment_hash.spl
- phishing_score.spl
- quarantined_emails.spl
- blocked_emails.spl
- sender_domain_analysis.spl
- suspicious_subjects.spl
- email_statistics.spl
- ioc_extraction.spl

---

## Severity Levels

| Score | Severity |
|--------|----------|
| 5 | Critical |
| 4 | High |
| 3 | Medium |
| 1-2 | Low |

---

## Response

- Quarantine Email
- Block Sender
- Block URL
- Block Attachment
- Notify SOC