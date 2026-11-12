# SOC Analyst Investigation Report — Apache Access Logs

## 1. Investigation Overview

**Project:** Web Server Log Analysis  
**Training Platform:** TryHackMe — Intro to Log Analysis  
**Tools:** macOS Terminal, Linux/Unix command-line utilities, Apache access logs  
**Investigation Type:** HTTP Traffic and Error Analysis

### Objective

Analyze a sample Apache web server access log to identify HTTP response patterns, frequently occurring IP addresses, and potentially suspicious requests.

## 2. Methodology

I used command-line utilities to examine the log file, count HTTP responses, identify frequently occurring source IP addresses, and investigate unsuccessful requests.

Commands used:

```bash
wc -l ~/Downloads/apache*.log
```

```bash
awk '{print $1}' ~/Downloads/apache*.log | sort | uniq -c | sort -nr | head
```

```bash
awk '$9 == 404 {print $1}' ~/Downloads/apache*.log | sort | uniq -c | sort -nr
```

```bash
grep '128.45.76.66' ~/Downloads/apache*.log
```

```bash
awk '$9 == 404 {print $7}' ~/Downloads/apache*.log | sort | uniq -c | sort -nr
```

```bash
awk '{print $9}' ~/Downloads/apache*.log | sort | uniq -c | sort -nr
```

## 3. Investigation Findings

### HTTP Response Analysis

| HTTP Status | Count | Percentage |
|---|---:|---:|
| 200 — OK | 52 | 73.2% |
| 404 — Not Found | 19 | 26.8% |
| Total | 71 | 100% |

The status-code analysis returned 71 requests. An earlier newline-based line count returned 70, which may indicate that the final log entry does not end with a newline. This difference requires verification.

### Most Frequently Requested IP Address

**IP Address:** `145.76.33.201`

**Requests:** 8

This IP address generated the highest number of requests in the analyzed sample.

### IP Address Investigation

**Investigated IP:** `128.45.76.66`

**Total requests:** 6  
**HTTP 404 responses:** 4  
**HTTP 200 responses:** 2

The IP address requested several resources, including:

- `/contact.php`
- `/about.php`
- `/index.php`
- `/login.php`

Four requests resulted in HTTP 404 errors.

### Most Common Missing Resources

| Resource | 404 Responses |
|---|---:|
| `/contact.php` | 8 |
| `/about.php` | 6 |
| `/login.php` | 4 |
| `/index.php` | 1 |

The `/contact.php` endpoint generated the highest number of 404 responses.

## 4. Security Assessment

The log sample contains repeated unsuccessful HTTP requests from multiple source IP addresses.

Possible explanations include:

- Requests for outdated or broken website links
- Automated web crawling
- Attempts to discover available web resources
- Website configuration problems

The available evidence does not establish malicious intent or confirm a security incident.

**Assessment:** Inconclusive — further investigation recommended.

## 5. Recommended Next Steps

1. Review additional access logs to determine whether the activity continues.
2. Compare timestamps and request sequences for unusual patterns.
3. Investigate repeated requests to nonexistent endpoints.
4. Review server configuration and application routing.
5. Correlate relevant events with other available security logs.

## 6. Skills Demonstrated

- Apache access log analysis
- Linux/Unix command-line investigation
- HTTP status-code interpretation
- IP address frequency analysis
- Log filtering using `awk` and `grep`
- Sorting and counting events
- Security investigation documentation
- Evidence-based analytical reasoning

## 7. Conclusion

This project provided practical experience investigating Apache web server activity using command-line tools.

I identified frequently occurring source IP addresses, analyzed HTTP response codes, examined unsuccessful requests, and documented findings.

The investigation demonstrates foundational skills relevant to entry-level Security Operations Center (SOC) analyst positions.

**Environment:** Authorized training dataset used for educational purposes.
