
# Project 4: Security Incident Response

## Project Overview

This project demonstrates the process of investigating and responding to a simulated cybersecurity incident affecting a small business.

The assessment follows a structured incident response process to identify suspicious activity, evaluate potential security impacts, recommend containment measures, and document recovery actions.

**Project Type:** Simulated Security Incident Investigation

**Role:** Junior SOC Analyst

**Environment:** Fictional Small Business

**Status:** In Progress

## Project Objectives

1. Identify indicators of a potential security incident.
2. Analyze suspicious account and network activity.
3. Determine the incident's preliminary severity.
4. Recommend containment and eradication actions.
5. Develop recovery and monitoring recommendations.
6. Document the investigation in a professional incident report.

## Incident Response Framework

This project uses the following incident response activities:

1. Preparation
2. Detection and Analysis
3. Containment
4. Eradication
5. Recovery
6. Post-Incident Review

## Skills Demonstrated

- Security Incident Identification
- Log Analysis
- Threat Investigation
- Incident Severity Assessment
- Incident Containment
- Security Documentation
- Incident Response Planning

## Assessment Status

Investigation Pending - Simulated Scenario

## Disclaimer

This project uses fictional security events and simulated evidence for educational purposes. No real business systems were accessed, investigated, or modified.


---

# Incident 001: Suspicious Account Login

## Incident Overview

**Incident ID:** IR-001

**Incident Type:** Suspicious Authentication Activity

**Environment:** Simulated Small Business

**Affected Asset:** Employee User Account

**Detection Method:** Authentication Log Review

**Investigation Status:** Open - Under Investigation

## Incident Scenario

A small business identified unusual authentication activity involving an employee account.

The security logs showed 15 failed login attempts within a 10-minute period, followed by one successful login at 2:14 AM from an unfamiliar IP address.

The employee's normal working hours are 8:00 AM to 5:00 PM.

When contacted, the employee stated that they were asleep during the successful login and did not recognize the activity.

These events suggest a possible unauthorized account access attempt and require further investigation.

## Initial Evidence

| Evidence | Observation |
|---|---|
| Failed Login Attempts | 15 |
| Failed Login Window | 10 minutes |
| Successful Login | 2:14 AM |
| Source IP Address | Unfamiliar; exact IP not provided |
| Employee Working Hours | 8:00 AM - 5:00 PM |
| Employee Confirmation | Did not recognize the login |
| Account Compromise | Suspected, not yet confirmed |

## Initial Investigation Notes

The repeated failed login attempts may indicate password guessing or another unauthorized authentication attempt.

The successful login following the failures raises concern that the account credentials may have been compromised.

However, the available evidence does not establish how the successful authentication occurred or whether the same source was responsible for the failed attempts.

Additional log analysis and account activity review are required before confirming the cause and scope of the incident.
