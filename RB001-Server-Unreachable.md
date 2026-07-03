# RB001 — Server Unreachable

**Category:** Infrastructure  
**Priority:** P2  
**Version:** 1.0  
**Last Updated:** July 2025  

---

## 1. Detection Symptoms
- Server not responding to ping
- Monitoring alert fired for host unreachable
- Services hosted on server returning connection timeout
- Users reporting inability to access applications

---

## 2. Immediate Triage Steps
1. Confirm alert is not a false positive — ping server from two different locations
2. Check monitoring dashboard for any related alerts (CPU, memory, disk)
3. Verify if scheduled maintenance is in progress
4. Check if other servers in same network segment are affected
5. Log incident in ServiceNow with Priority P2

---

## 3. Escalation Path
| Time | Action |
|------|--------|
| 0–5 mins | L1 analyst attempts basic triage |
| 5–15 mins | Escalate to L2 Infrastructure team |
| 15–30 mins | Escalate to Infrastructure Lead |
| 30+ mins | Notify Service Delivery Manager |

---

## 4. Resolution Procedure
1. Attempt remote reboot via IPMI/iDRAC console
2. If remote reboot fails — raise request for physical data centre access
3. Check server hardware health (CPU, memory, disk, NIC)
4. Review system logs for errors before server went unreachable
5. Restore services once server is back online
6. Confirm with affected teams that services are restored

---

## 5. Post-Resolution Validation
- Ping server and confirm response
- Check all hosted services are running
- Verify monitoring alerts have cleared
- Confirm with users that access is restored

---

## 6. Prevention Recommendations
- Enable automated reboot on hardware failure
- Set up redundant monitoring with alerting
- Implement server health checks every 5 minutes
- Review hardware warranty and replacement schedule
