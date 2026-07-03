# RB002 — High CPU Alert

**Category:** Infrastructure  
**Priority:** P2  
**Version:** 1.0  
**Last Updated:** July 2025  

---

## 1. Detection Symptoms
- Monitoring alert fired for CPU usage above 90%
- Server response time degraded
- Applications running slow or timing out
- Users reporting poor performance

---

## 2. Immediate Triage Steps
1. Log into monitoring dashboard and confirm CPU spike
2. Check which process is consuming high CPU
3. Verify if spike is sustained or intermittent
4. Check if any deployments or jobs ran recently
5. Log incident in ServiceNow with Priority P2

---

## 3. Escalation Path
| Time | Action |
|------|--------|
| 0–5 mins | L1 analyst identifies high CPU process |
| 5–15 mins | Escalate to L2 if process cannot be identified |
| 15–30 mins | Escalate to Application or Infrastructure Lead |
| 30+ mins | Notify Service Delivery Manager |

---

## 4. Resolution Procedure
1. Identify the process consuming high CPU using Task Manager or top command
2. Check if process is legitimate or a runaway process
3. If runaway — kill the process after confirming with application owner
4. If legitimate — check if server needs to be scaled up
5. Restart affected application service if required
6. Monitor CPU for 15 minutes post fix to confirm stabilisation

---

## 5. Post-Resolution Validation
- Confirm CPU usage is back below 70%
- Verify all applications are responding normally
- Check monitoring alerts have cleared
- Confirm with users that performance is restored

---

## 6. Prevention Recommendations
- Set CPU alert threshold at 80% for early warning
- Schedule regular review of resource intensive jobs
- Implement auto-scaling for critical servers
- Review and optimise application code for CPU efficiency
