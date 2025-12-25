## Windows Authentication Log Analysis

- Event ID 4625 used to detect failed logins
- Event ID 4624 used to identify successful logins
- Logon Type 10 indicates RDP access

### Detection Patterns
- Multiple failures from same IP → Brute Force
- Failures across many users → Password Spray
- Successful login after failures → High risk
