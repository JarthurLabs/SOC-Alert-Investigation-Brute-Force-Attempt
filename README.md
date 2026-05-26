# SOC Alert Investigation: Brute Force Login Attempt

## Overview

This repository contains a SOC-style alert investigation using synthetic authentication logs. The investigation reviews repeated failed logins followed by a successful login, builds a timeline, documents evidence, determines alert disposition, and recommends containment actions.

The focus is analyst workflow: validate the alert, review evidence, build a timeline, explain why the activity is suspicious, and document next steps.

> All users, timestamps, IP addresses, and logs are synthetic. The external IP address uses documentation-safe address space.

---

## Scenario

A monitoring rule triggered after multiple failed login attempts against one user account were followed by a successful login from the same source IP. The SOC analyst needs to determine whether this is likely brute force activity, false positive behavior, or a confirmed suspicious event requiring escalation.

The investigation answers five questions:

1. What triggered the alert?
2. What evidence supports the alert?
3. Did a successful login occur after failed attempts?
4. What is the likely impact?
5. What containment and follow-up actions are recommended?

---

## Target Roles

| Role | Why This Repository Fits |
|---|---|
| SOC Analyst | Shows alert triage, timeline building, event review, and containment notes |
| Cybersecurity Analyst | Demonstrates evidence-based investigation and incident documentation |
| Incident Response Analyst, beginner | Shows containment logic and escalation criteria |
| Security Implementation Specialist | Connects alert findings to MFA and account-control improvements |

---

## Core Deliverables

| Area | Deliverables |
|---|---|
| Alert Triage | Alert summary, initial severity, affected user, source IP |
| Log Analysis | Synthetic authentication events and timeline |
| Investigation Evidence | Source IP analysis, event ID review, triage decision |
| Detection Logic | SIEM-style query examples and tuning notes |
| Response | Containment checklist and escalation recommendation |
| Reporting | Incident summary and final analyst report |

---

## Alert Summary

![Alert Summary](./screenshots/alert-summary.svg)

---

## Authentication Timeline

The timeline shows why the activity was treated as suspicious: repeated failures followed by successful authentication.

![Authentication Timeline](./screenshots/authentication-timeline.svg)

---

## Source IP Analysis

The source IP review shows repeated attempts from the same external documentation-safe address.

![Source IP Analysis](./screenshots/source-ip-analysis.svg)

---

## Triage Decision Flow

![Triage Decision Flow](./screenshots/triage-decision.svg)

---

## Containment Checklist

![Containment Checklist](./screenshots/containment-checklist.svg)

---

## Repository Structure

```text
.
├── README.md
├── CHANGELOG.md
├── COMMIT_GUIDE.md
├── alert-triage/
├── data/
├── evidence/
├── detection-logic/
├── response/
├── reports/
├── screenshots/
└── templates/
```

---

## Key Evidence Files

| File | Purpose |
|---|---|
| `data/authentication-events.csv` | Synthetic event log sample |
| `data/investigation-timeline.csv` | Timeline of suspicious activity |
| `data/triage-summary.csv` | Alert metadata and disposition |
| `data/containment-checklist.csv` | Response actions |
| `detection-logic/siem-query-examples.md` | SIEM-style search examples |
| `reports/final-report.md` | Completed analyst report |

---

## Analyst Conclusion

The activity is consistent with a brute-force or password-guessing attempt because one account received multiple failed logins from the same external source followed by a successful login. The successful login increases severity and requires account validation, password reset, active session revocation, and MFA review.

---

## Limitations

This is a synthetic SOC investigation. It does not contain real logs, real users, real IP addresses, malware, or production incident data.
