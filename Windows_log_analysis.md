## Windows Authentication Log Analysis

Windows systems record authentication activity in the Security Event Logs.
SOC analysts rely on these logs to identify suspicious login behavior.

---

## Important Event IDs

### Event ID 4625 – Failed Logon
This event indicates that a login attempt has failed.
Common reasons include incorrect passwords or invalid usernames.

SOC analysts monitor:
- Frequency of failures
- Source IP address
- Logon type
- Usernames being targeted

---

### Event ID 4624 – Successful Logon
This event indicates that a login attempt was successful.
It is important to correlate successful logons with previous failures.

A successful login after multiple failures is considered high risk.

---

## Logon Types (SOC Relevant)

- Logon Type 2: Local login
- Logon Type 3: Network login
- Logon Type 10: Remote login (RDP)

Logon Type 10 is especially sensitive because RDP is a common attack target.

---

## Detection Patterns

### Brute Force Attack
- Multiple failed logins
- Same user account
- Same source IP
- Short time period

### Password Spraying
- Few login attempts per user
- Multiple user accounts
- Same source IP
- Longer time window

---

## SOC Decision Making
SOC analysts do not react to a single failed login.
They look for patterns, repetition, and context before escalating.
