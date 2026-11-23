
# Splunk Queries — SIEM Threat Detection Lab

## Lab Overview

This project uses fictional authentication logs to investigate suspicious login activity and practice foundational Security Operations Center (SOC) skills.

## Query 1 — View Authentication Events

```spl
index=main sourcetype="csv"
| table _time username source_ip event_type status
```

**Purpose:** Display authentication events for investigation.

## Query 2 — Identify Failed Login Attempts

```spl
index=main sourcetype="csv" status="failure"
| stats count by username source_ip
| sort - count
```

**Purpose:** Identify accounts and source IP addresses associated with failed login attempts.

## Query 3 — Detect Repeated Failed Logins

```spl
index=main sourcetype="csv" status="failure"
| stats count as failed_attempts by username source_ip
| where failed_attempts >= 3
| sort - failed_attempts
```

**Purpose:** Identify potential brute-force login activity.

## Query 4 — Investigate Successful Logins

```spl
index=main sourcetype="csv" status="success"
| table _time username source_ip status
```

**Purpose:** Review successful authentication events for potentially suspicious activity.

## Investigation Notes

These queries are prepared for testing after the sample authentication logs are imported into Splunk.

The index and sourcetype may need to be adjusted to match the actual Splunk configuration.
