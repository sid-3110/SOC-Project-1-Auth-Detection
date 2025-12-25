## SOC Detection Logic

This section explains the investigation logic used by a SOC L1 analyst.

---

## Detection Rules (Conceptual)

- If multiple failed login attempts occur from the same IP in a short
  time period, it may indicate a brute force attack.

- If one IP attempts to authenticate against many different user accounts,
  it may indicate password spraying.

- If a successful login occurs after multiple failures, the alert should
  be escalated immediately.

---

## Context-Based Analysis
SOC decisions are always based on context, such as:
- Time of activity
- User role (admin vs normal user)
- Internal vs external IP
- Historical behavior

---

## Escalation Criteria
An alert should be escalated when:
- Repeated failures are observed
- High-risk logon types are involved
- Privileged accounts are targeted
