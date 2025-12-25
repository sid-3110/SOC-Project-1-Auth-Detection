## Linux SSH Authentication Log Analysis

- Log file: /var/log/auth.log
- Failed password entries indicate login failures
- Accepted password entries indicate successful login

### Detection Patterns
- Repeated failures from same IP → SSH brute force
- Unknown external IPs require investigation
