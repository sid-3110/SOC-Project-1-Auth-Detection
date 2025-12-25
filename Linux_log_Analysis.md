## Linux SSH Authentication Log Analysis

Linux systems store authentication logs that record SSH login activity.
These logs are critical for detecting unauthorized access attempts.

---

## Log File Location
- Debian/Ubuntu: /var/log/auth.log
- RedHat/CentOS: /var/log/secure

---

## Important Log Entries

### Failed SSH Login
Log entries containing:
- "Failed password"
- Username
- Source IP address

These indicate unsuccessful SSH login attempts.

---

### Successful SSH Login
Log entries containing:
- "Accepted password"
- Username
- Source IP address

Successful logins should be validated against known administrators
and expected IP addresses.

---

## Detection Patterns

### SSH Brute Force Attack
- Repeated "Failed password" messages
- Same external IP address
- Multiple usernames or repeated attempts

### Normal SSH Behavior
- Few attempts
- Known administrator account
- Known internal or trusted IP address

---

## SOC Perspective
SOC analysts differentiate between human mistakes and automated attacks
by analyzing frequency, timing, and source IP addresses.
