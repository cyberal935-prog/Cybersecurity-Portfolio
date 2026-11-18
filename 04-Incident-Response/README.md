
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


## Preliminary Incident Severity Assessment

**Incident ID:** IR-001

**Preliminary Severity:** High

**Assessment Status:** Preliminary - Further Investigation Required

### Severity Justification

The incident has been assigned a preliminary High severity rating due to suspicious authentication activity involving an employee account.

The following indicators support this assessment:

1. Fifteen failed login attempts occurred within a 10-minute period.
2. A successful login occurred at 2:14 AM outside normal business hours.
3. The successful login originated from an unfamiliar IP address.
4. The employee confirmed that they did not recognize the login activity.
5. The sequence of events raises concern about possible unauthorized account access.

### Potential Security Impact

If the account has been compromised, an unauthorized individual may be able to:

- Access business systems and resources available to the employee.
- View or obtain sensitive business information.
- Perform unauthorized actions using the employee's identity.
- Attempt additional account access or privilege escalation.

These impacts are potential risks and have not been confirmed.

### Why Critical Severity Was Not Assigned

Critical severity was considered because a successful login occurred under suspicious circumstances.

However, the available evidence does not confirm:

- Compromise of privileged or administrative accounts.
- Unauthorized access to sensitive information.
- Data theft or exfiltration.
- Widespread system compromise.
- Major business disruption.

Without evidence of severe impact or additional critical risk factors, a preliminary High severity rating is more appropriate.

### Recommended Response Priority

**Response Priority:** High - Urgent Investigation

Recommended initial actions include:

1. Notify the security team or designated incident responder.
2. Preserve relevant authentication and account activity logs.
3. Investigate the successful login and associated source IP address.
4. Review account permissions and recent activity.
5. Consider temporarily disabling the account or revoking active sessions to prevent further unauthorized access.
6. Require a secure password reset and verify multifactor authentication settings.
7. Reassess severity as additional evidence becomes available.

### Severity Assessment Conclusion

The suspicious authentication activity represents a potential account compromise requiring urgent investigation and protective action.

The incident will remain classified as High severity until additional evidence supports escalation or reduction.

**Final Severity:** Not Yet Determined

**Investigation Status:** Open - Under Investigation


## Incident Containment and Response Plan

**Incident ID:** IR-001

**Incident Severity:** High (Preliminary)

**Response Phase:** Containment

**Containment Status:** Proposed - Not Implemented

### Containment Objectives

The primary objectives of containment are to prevent further unauthorized account access, protect business resources, and preserve evidence for investigation.

### Immediate Containment Actions

1. Notify the designated security incident response team.
2. Preserve authentication logs and relevant security alerts.
3. Temporarily disable the affected employee account if authorized and operationally appropriate.
4. Revoke active sessions and authentication tokens associated with the affected account.
5. Require a secure password reset through a trusted recovery process.
6. Review and strengthen multifactor authentication (MFA) settings.
7. Monitor for additional suspicious login attempts or related account activity.

### Evidence Preservation

Before making changes where feasible, the incident responder should preserve:

- Authentication logs showing failed and successful login attempts.
- Source IP addresses associated with authentication events.
- Login timestamps and relevant time zone information.
- Account activity and security alerts.
- Device information and session details, if available.
- Relevant changes to account permissions or security settings.

Evidence should be stored securely with restricted access and documented collection times to support investigation.

### Account Protection Measures

The affected account should be treated as potentially compromised until further investigation establishes otherwise.

Recommended protective measures include:

- Resetting the account password using a secure process.
- Revoking suspicious or unrecognized sessions.
- Verifying registered MFA methods and recovery information.
- Reviewing recent account changes and access permissions.
- Restoring access only after appropriate security checks.

### Communication and Escalation

The designated incident responder should notify the appropriate IT or security personnel and coordinate with the affected employee.

The incident should be escalated if evidence reveals:

- Unauthorized access to sensitive information.
- Compromise of privileged accounts.
- Additional affected users or systems.
- Evidence of data exfiltration.
- Significant operational disruption.

### Containment Verification

After authorized containment actions are completed, the security team should verify that:

1. Previously active suspicious sessions are no longer valid.
2. Unauthorized login attempts are blocked or appropriately monitored.
3. Account credentials and MFA methods have been secured.
4. No additional suspicious account activity is detected during the monitoring period.
5. Evidence remains available for further investigation.

### Containment Assessment Conclusion

The proposed containment plan prioritizes account protection, evidence preservation, and continued monitoring.

No containment actions have been executed as part of this simulated project.

**Containment Status:** Pending Implementation

**Incident Status:** Open - Investigation Ongoing
