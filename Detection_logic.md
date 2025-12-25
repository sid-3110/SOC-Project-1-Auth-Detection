## SOC Detection Logic

- Repeated failed logins from same IP → Investigate
- Same IP attempting multiple users → Password Spray
- Success after failures → Escalate immediately
- Context (time, user role, IP) decides action
