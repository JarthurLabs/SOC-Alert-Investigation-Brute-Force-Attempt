# Final Report: SOC Alert Investigation: Brute Force Login Attempt

## Executive Summary

A SOC-style investigation using synthetic authentication logs to triage failed logins, build a timeline, identify suspicious IP behavior, and recommend containment and hardening steps.

The main purpose of this project is to demonstrate practical cybersecurity judgment. The project uses synthetic data and a realistic small-business scenario to show how security work should be documented: scope, evidence, findings, impact, and recommendations.

## Scope

- Environment: Synthetic small-business environment
- Data classification: Public-safe simulated data
- Objective: Identify security risks and produce actionable recommendations
- Out of scope: Real client data, exploitation, malware execution, unauthorized scanning

## Methodology

1. Reviewed the scenario and defined the security objective.
2. Examined the provided synthetic data.
3. Identified findings and assigned practical severity.
4. Documented impact in plain business language.
5. Recommended remediation steps.
6. Summarized how the work maps to entry-level cybersecurity responsibilities.

## Findings

### Finding 1: 42 failed logins against one account in 9 minutes

- **Severity / Type:** High
- **Impact:** Pattern strongly suggests password guessing.
- **Recommended Action:** Validate the issue, assign an owner, prioritize based on business impact, document remediation, and retest.

### Finding 2: One successful login after failures

- **Severity / Type:** High
- **Impact:** Potential account compromise requiring validation.
- **Recommended Action:** Validate the issue, assign an owner, prioritize based on business impact, document remediation, and retest.

### Finding 3: Login source is geolocated outside normal user region

- **Severity / Type:** Medium
- **Impact:** Anomaly increases suspicion.
- **Recommended Action:** Validate the issue, assign an owner, prioritize based on business impact, document remediation, and retest.

### Finding 4: No MFA challenge recorded

- **Severity / Type:** Medium
- **Impact:** Control gap increases account takeover risk.
- **Recommended Action:** Validate the issue, assign an owner, prioritize based on business impact, document remediation, and retest.

### Finding 5: Alert lacked owner metadata

- **Severity / Type:** Low
- **Impact:** Slowed triage and escalation.
- **Recommended Action:** Validate the issue, assign an owner, prioritize based on business impact, document remediation, and retest.

## Recommendations

- Prioritize high-impact issues first.
- Assign each finding to a clear owner.
- Track remediation status.
- Retest after changes are made.
- Keep documentation concise enough for business stakeholders and detailed enough for technical follow-up.

## What This Demonstrates to Employers

This project shows how I think like an analyst: confirm the alert, collect evidence, determine whether the activity is suspicious, document impact, and recommend practical next steps.

## Resume Bullet Option

Built a cybersecurity portfolio project simulating soc alert investigation: brute force login attempt, documenting scope, evidence, findings, risk impact, and remediation recommendations using public-safe synthetic data.
