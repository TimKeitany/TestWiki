# 🚨 Incident Report: [Short Title]
**Date:** YYYY-MM-DD  
**Duration:** HH:MM to HH:MM  
**Severity:** Low / Medium / High / Critical  
**Reported by:** [Person or Team Name]

---

## 🧠 Summary
Brief explanation of what went wrong. Write as if you're explaining to someone outside your team.

> Example:  
> Between 10:34 AM and 11:12 AM EAT, the public API experienced timeouts affecting 40% of traffic, due to a misconfigured rate-limiter deployed in the latest release.

---

## 🔍 Impact
- Which users, systems, or teams were affected?
- Estimated user or revenue impact
- SLA/SLO breaches (if any)

---

## 📅 Timeline (UTC / Local Time)
| Time       | Event |
|------------|-------|
| 10:34 AM   | Alert triggered: API latency > 2s |
| 10:36 AM   | Engineer began investigation |
| 10:50 AM   | Rollback initiated |
| 11:12 AM   | Incident resolved |

---

## 🛠️ Root Cause
Explain what caused the incident.

> Example:  
> A new version of the rate-limiter was deployed without preserving old configuration defaults, causing all requests over 100 per second to be rejected.

---

## ✅ Resolution
What steps were taken to restore service?

> - Rolled back to stable release `v1.9.3`
> - Flushed invalid cache
> - Restarted 2 backend nodes

---

## 🔁 Corrective Actions & Follow-Up Tasks

| Owner | Action Item | Priority | Due Date |
|-------|-------------|----------|----------|
| DevOps | Add CI validation for rate-limiter config | High | 2025-06-24 |
| Eng Team | Add rollback playbook to runbook | Medium | 2025-06-30 |

---

## 📚 Learnings
What can we do better next time?

- **What went well:** Quick detection, fast rollback
- **What didn't go well:** Missed config validation, unclear ownership
- **How to improve:** Document release steps better; implement config checks

---

## 📎 Attachments
- [Grafana dashboard screenshot](#)
- [Slack thread](#)
- [PagerDuty Incident #](#)

---

> _This postmortem is blameless. Its goal is to learn and improve, not assign blame._
