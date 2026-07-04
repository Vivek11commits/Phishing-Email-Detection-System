# Phishing Email Investigation Report

## Incident Summary

A phishing email was detected during routine email monitoring. The email contained a suspicious sender domain, malicious URL, and a potentially dangerous attachment.

---

## Alert Details

- Alert Type: Phishing Email
- Severity: High
- Detection Time: 2026-07-04
- Status: Investigated

---

## Indicators of Compromise (IOCs)

### Sender Email
security-update@micr0soft-support.com

### Sender Domain
micr0soft-support.com

### Source IP
185.244.25.33

### URL
http://micr0soft-support.com/reset

### Attachment

reset.html

### Attachment Hash

44d88612fea8a8f36de82e1278abb02f

---

## Investigation Findings

- SPF validation failed.
- DKIM validation failed.
- DMARC validation failed.
- Email contained a non-HTTPS URL.
- Sender domain impersonated Microsoft.
- HTML attachment could be used for credential harvesting.

---

## Actions Taken

- Email quarantined.
- Sender blocked.
- URL reported as malicious.
- IOC added to blocklist.
- User notified.

---

## Recommendations

- Block malicious sender domain.
- Block source IP.
- Block malicious URL.
- Update email filtering rules.
- Conduct user phishing awareness training.

---

## Conclusion

The email was confirmed as a phishing attempt and successfully quarantined before user interaction.